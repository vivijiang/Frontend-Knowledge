
Why we decide to use Angular?
================================
- Because It’s awesome? No
- Because it’s pure client side solution? No
- Because it’s not server-side rendering? No
- Because of code quality.
- Because of productivity.


5 major components
======================
- Directives
- Controllers
- Scopes
- Services
- Dependency Injection

DI
======
- through constructor
- name mathes (variable $scope matches $scope service)
- the moudule should be requried into the current module.
- “inline annotation” to avoid variable name being modified while doing js "minify".


Services
==================
- Singleton
- Examples
    - $http
    - $cookies
- write our own


Service, factory, provider
===============================
- service and factory are both implemented by provider under the hood.
- http://stackoverflow.com/questions/15666048/angular-js-service-vs-provider-vs-factory/17944367#17944367


Code organization
=====================
##code organization 1
- css/
- img/
- js/
	- app.js
	- controllers.js
	- directives.js
	- filters.js
	- services.js
- lib/
- partials/

##code organization 2
- controllers/
	- LoginController.js
	- RegistrationController.js
	- ProductDetailController.js
	- SearchResultsController.js
- directives.js
- filters.js
- models/
	- CartModel.js
	- ProductModel.js
	- SearchResultsModel.js
	- UserModel.js
- services/
	- CartService.js
	- UserService.js
	- ProductService.js


## Code organization 3: Modurity
- cart/
	- CartModel.js
	- CartService.js
- common/
	- directives.js
	- filters.js
- product/
	- search/
		- SearchResultsController.js
		- SearchResultsModel.js
	- ProductDetailController.js
	- ProductModel.js
	- ProductService.js
- user/
	- LoginController.js
	- RegistrationController.js
	- UserModel.js
	- UserService.js


Tips
====================
- keep your code organized
- keep controllers simple/thin
- if you end writing $(element) somewhere in your controller, it's a indication you need a directive.
- Business logic belongs to models.
- create facade to interact with servers.
- sepaate server interaction and error handling from the model.
- Leverage provider configuration
- Automate your workflow(todo: will set it up)
- Yeoman: https://github.com/yeoman/generator-angular
- Grunt/gulp.js
- bower


Links
============
Must Read
-----------
- http://www.ng-newsletter.com/posts/how-to-learn-angular.html
- https://github.com/jmcunningham/AngularJS-Learning
- http://stackoverflow.com/questions/14994391/how-do-i-think-in-angularjs-if-i-have-a-jquery-background?rq=1



- http://cliffmeyers.com/blog/2013/4/21/code-organization-angularjs-javascript
- https://github.com/yeoman/generator-angular
- http://joelhooks.com/blog/2013/05/22/lessons-learned-kicking-off-an-angularjs-project/
- http://trochette.github.io/Angular-Design-Patterns-Best-Practices/#/intro
- cheatsheet: http://www.cheatography.com/proloser/cheat-sheets/angularjs/
- build: https://medium.com/@dickeyxxx/best-practices-for-building-angular-js-apps-266c1a4a6917
- Performance: http://blog.scalyr.com/2013/10/angularjs-1200ms-to-35ms/


What about jQuery?
======================
- Must read: http://stackoverflow.com/questions/14994391/how-do-i-think-in-angularjs-if-i-have-a-jquery-background?rq=1
- Don't design your page, and then change it with DOM manipulations
- Don't augment jQuery with AngularJS
- Always think in terms of architecture
- Test-driven development - always
- Conceptually, directives are not packaged jQuery
- Conclusion: Don't even use jQuery. Don't even include it. It will hold you back.

