1. iframe

  data.json
  ```json
  {
    "success": true,
    "data": "operation succeeded!"
  }
  ```
  get
  ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <title>Title</title>
      <script>
          function load() {
              var iframe = document.getElementById('iframe'),
                      content = document.getElementById('content');
              content.innerHTML = 'Loading...';
              iframe.src = 'data.json';
              iframe.onload = function() {
                  var data = iframe.contentDocument.body.innerText,
                          json = JSON.parse(data);
                  if (json.success) {
                      content.innerHTML = json.data;
                  }
              };
          }
      </script>
  </head>
  <body>
  <button onclick="load()">Load</button>
  <div id="content"></div>
  <iframe id="iframe" style="display:none"></iframe>
  </body>
  </html>
  ```
  post
  ```javascript
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <title>Title</title>
      <script>
          function save() {
              var content = document.getElementById('content');
              content.innerHTML = 'Loading...';
              document.getElementById('form').submit();
          }
          window.onload = function() {
              var iframe = document.getElementById('iframe');
              iframe.onload = function() {
                  var data = iframe.contentDocument.body.innerText,
                          json = JSON.parse(data);
                  if (json.success) {
                      content.innerHTML = json.data;
                  }
              };
          };
      </script>
  </head>
  <body>
  <div id="content"></div>
  <form id="form" target="iframe" action="data.json" method="post">
      name:<input type="text">
      <button onclick="save();return false;">Submit</button>
  </form>
  <iframe id="iframe" name="iframe" style="display:none"></iframe>
  </body>
  </html>
  ```

2. script tag
  ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <title>Title</title>
      <script>
          function load() {
              var content = document.getElementById('content');
              content.innerHTML = 'Loading...';
  
              var script = document.createElement('script');
              script.src = 'cb.js';
              document.body.appendChild(script);
          }
  
          function callback(response) {
              response = JSON.parse(response);
              if (response.success) {
                  document.getElementById('content').innerHTML = response.data;
              }
          }
  
      </script>
  </head>
  <body>
  <div id="content"></div>
  <button onclick="load();">Submit</button>
  </body>
  </html>
  ```

3. image, style sheet

4. XMLHttpRequest
  ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <title>Title</title>
      <script>
          function load() {
              var xhr = new XMLHttpRequest();
              xhr.onreadystatechange = function() {
                  if (xhr.readyState == 4 && xhr.status == 200) {
                      var response = JSON.parse(xhr.responseText);
                      if (response.success) {
                          document.getElementById("content").innerHTML = response.data;
                      }
                  }
              };
              xhr.open("GET", "data.json", true);
              xhr.send();
          }
      </script>
  </head>
  <body>
  <div id="content"></div>
  <button onclick="load();">Submit</button>
  </body>
  </html>
  ```