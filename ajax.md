1. iframe

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
