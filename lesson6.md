#Go over
1. SenchaMVC
1. Hack [http://www.zolo.ca/vaughan-real-estate/28-thomson-creek-boulevard](http://www.zolo.ca/vaughan-real-estate/28-thomson-creek-boulevard)
1. Debug

        function notifyLoginSuccess(resolve, result) {
          if(angular.isDefined(result.license))
            $localStorage.licenseCode= result.license;
          if(angular.isDefined(result.fl))
            $localStorage.flag = result.fl;
          if(angular.isDefined(result.fl2))
            $localStorage.flag2 = result.fl2;
          if(angular.isDefined(result.pr))
            $localStorage.privilege = result.pr;
          if(angular.isDefined(result.pr2))
            $localStorage.privilege2 = result.pr2;
          UserService.set(result);
          LicenseService.set(result.license);

          resolve(UserService.get());
          $rootScope.$broadcast('loggedIn', UserService.get());
          if(credentials && credentials.password && credentials.password.slice(0, 3) == 'tmp') {
            open('changePassword')();
          }
        }

#New
1. ExtJS
    1. Form validation
    1. set/get value
1. AngularJS
    1. module
    1. dependency injection
    1. deferred/promise pattern
    1. two-way data biding
