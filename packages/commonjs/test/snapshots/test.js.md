# Snapshot report for `test/test.js`

The actual snapshot is saved in `test.js.snap`.

Generated by [AVA](https://avajs.dev).

## produces optimized code when importing esm with a known default export

> Snapshot 1

    `'use strict';␊
    ␊
    function getDefaultExportFromCjs (x) {␊
    	return x && x.__esModule && Object.prototype.hasOwnProperty.call(x, 'default') ? x['default'] : x;␊
    }␊
    ␊
    var require$$0 = "default";␊
    ␊
    var main$1;␊
    var hasRequiredMain;␊
    ␊
    function requireMain () {␊
    	if (hasRequiredMain) return main$1;␊
    	hasRequiredMain = 1;␊
    	main$1 = require$$0;␊
    	return main$1;␊
    }␊
    ␊
    var mainExports = requireMain();␊
    var main = /*@__PURE__*/getDefaultExportFromCjs(mainExports);␊
    ␊
    module.exports = main;␊
    `

## produces optimized code when importing esm without a default export

> Snapshot 1

    `'use strict';␊
    ␊
    function getDefaultExportFromCjs (x) {␊
    	return x && x.__esModule && Object.prototype.hasOwnProperty.call(x, 'default') ? x['default'] : x;␊
    }␊
    ␊
    function getAugmentedNamespace(n) {␊
      if (Object.prototype.hasOwnProperty.call(n, '__esModule')) return n;␊
      var f = n.default;␊
    	if (typeof f == "function") {␊
    		var a = function a () {␊
    			var isInstance = false;␊
          try {␊
            isInstance = this instanceof a;␊
          } catch {}␊
    			if (isInstance) {␊
            return Reflect.construct(f, arguments, this.constructor);␊
    			}␊
    			return f.apply(this, arguments);␊
    		};␊
    		a.prototype = f.prototype;␊
      } else a = {};␊
      Object.defineProperty(a, '__esModule', {value: true});␊
    	Object.keys(n).forEach(function (k) {␊
    		var d = Object.getOwnPropertyDescriptor(n, k);␊
    		Object.defineProperty(a, k, d.get ? d : {␊
    			enumerable: true,␊
    			get: function () {␊
    				return n[k];␊
    			}␊
    		});␊
    	});␊
    	return a;␊
    }␊
    ␊
    const value = "value";␊
    ␊
    var esm = /*#__PURE__*/Object.freeze({␊
    	__proto__: null,␊
    	value: value␊
    });␊
    ␊
    var require$$0 = /*@__PURE__*/getAugmentedNamespace(esm);␊
    ␊
    var main$1;␊
    var hasRequiredMain;␊
    ␊
    function requireMain () {␊
    	if (hasRequiredMain) return main$1;␊
    	hasRequiredMain = 1;␊
    	main$1 = require$$0;␊
    	return main$1;␊
    }␊
    ␊
    var mainExports = requireMain();␊
    var main = /*@__PURE__*/getDefaultExportFromCjs(mainExports);␊
    ␊
    module.exports = main;␊
    `

## handles array destructuring assignment

> Snapshot 1

    `'use strict';␊
    ␊
    Object.defineProperty(exports, '__esModule', { value: true });␊
    ␊
    function getDefaultExportFromCjs (x) {␊
    	return x && x.__esModule && Object.prototype.hasOwnProperty.call(x, 'default') ? x['default'] : x;␊
    }␊
    ␊
    var main$1 = {};␊
    ␊
    /* eslint-disable */␊
    ␊
    var hasRequiredMain;␊
    ␊
    function requireMain () {␊
    	if (hasRequiredMain) return main$1;␊
    	hasRequiredMain = 1;␊
    	function shuffleArray(array) {␊
    	  for (let i = array.length - 1; i > 0; i--) {␊
    	    const j = Math.floor(Math.random() * (i + 1));␊
    	    [array[i], array[j]] = [array[j], array[i]];␊
    	  }␊
    	}␊
    ␊
    	main$1.shuffleArray = shuffleArray;␊
    	return main$1;␊
    }␊
    ␊
    var mainExports = requireMain();␊
    var main = /*@__PURE__*/getDefaultExportFromCjs(mainExports);␊
    ␊
    exports.default = main;␊
    `

## can spread an object into module.exports

> Snapshot 1

    `'use strict';␊
    ␊
    function getDefaultExportFromCjs (x) {␊
    	return x && x.__esModule && Object.prototype.hasOwnProperty.call(x, 'default') ? x['default'] : x;␊
    }␊
    ␊
    var main$1;␊
    var hasRequiredMain;␊
    ␊
    function requireMain () {␊
    	if (hasRequiredMain) return main$1;␊
    	hasRequiredMain = 1;␊
    	const obj = {␊
    	  a: 'b',␊
    	  b: 'c'␊
    	};␊
    ␊
    	main$1 = {␊
    	  ...obj␊
    	};␊
    	return main$1;␊
    }␊
    ␊
    var mainExports = requireMain();␊
    var main = /*@__PURE__*/getDefaultExportFromCjs(mainExports);␊
    ␊
    module.exports = main;␊
    `

## does not transform typeof exports for mixed modules

> Snapshot 1

    `var foo$1;␊
    var hasRequiredFoo;␊
    ␊
    function requireFoo () {␊
    	if (hasRequiredFoo) return foo$1;␊
    	hasRequiredFoo = 1;␊
    	foo$1 = 21;␊
    	return foo$1;␊
    }␊
    ␊
    const foo = requireFoo();␊
    ␊
    if (typeof exports !== 'undefined') {␊
      throw new Error('There should be no global exports in an ES module');␊
    }␊
    ␊
    export { foo as default };␊
    `

## handles when an imported dependency of an ES module changes type

> Snapshot 1

    `'use strict';␊
    ␊
    const dep = 'esm';␊
    ␊
    module.exports = dep;␊
    `

> Snapshot 2

    `'use strict';␊
    ␊
    var dep$1 = {};␊
    ␊
    var hasRequiredDep;␊
    ␊
    function requireDep () {␊
    	if (hasRequiredDep) return dep$1;␊
    	hasRequiredDep = 1;␊
    	dep$1.dep = 'cjs';␊
    	return dep$1;␊
    }␊
    ␊
    var depExports = requireDep();␊
    ␊
    var dep = depExports.dep;␊
    ␊
    module.exports = dep;␊
    `

> Snapshot 3

    `'use strict';␊
    ␊
    var dep$1 = {};␊
    ␊
    var hasRequiredDep;␊
    ␊
    function requireDep () {␊
    	if (hasRequiredDep) return dep$1;␊
    	hasRequiredDep = 1;␊
    	dep$1.dep = 'cjs'; dep$1.dep += requireDep().dep;␊
    	return dep$1;␊
    }␊
    ␊
    var depExports = requireDep();␊
    ␊
    var dep = depExports.dep;␊
    ␊
    module.exports = dep;␊
    `

## handles when a required dependency of a CJS module changes type

> Snapshot 1

    `'use strict';␊
    ␊
    function getDefaultExportFromCjs (x) {␊
    	return x && x.__esModule && Object.prototype.hasOwnProperty.call(x, 'default') ? x['default'] : x;␊
    }␊
    ␊
    function getAugmentedNamespace(n) {␊
      if (Object.prototype.hasOwnProperty.call(n, '__esModule')) return n;␊
      var f = n.default;␊
    	if (typeof f == "function") {␊
    		var a = function a () {␊
    			var isInstance = false;␊
          try {␊
            isInstance = this instanceof a;␊
          } catch {}␊
    			if (isInstance) {␊
            return Reflect.construct(f, arguments, this.constructor);␊
    			}␊
    			return f.apply(this, arguments);␊
    		};␊
    		a.prototype = f.prototype;␊
      } else a = {};␊
      Object.defineProperty(a, '__esModule', {value: true});␊
    	Object.keys(n).forEach(function (k) {␊
    		var d = Object.getOwnPropertyDescriptor(n, k);␊
    		Object.defineProperty(a, k, d.get ? d : {␊
    			enumerable: true,␊
    			get: function () {␊
    				return n[k];␊
    			}␊
    		});␊
    	});␊
    	return a;␊
    }␊
    ␊
    const dep = 'esm';␊
    ␊
    var dep$1 = /*#__PURE__*/Object.freeze({␊
    	__proto__: null,␊
    	dep: dep␊
    });␊
    ␊
    var require$$0 = /*@__PURE__*/getAugmentedNamespace(dep$1);␊
    ␊
    var main$1;␊
    var hasRequiredMain;␊
    ␊
    function requireMain () {␊
    	if (hasRequiredMain) return main$1;␊
    	hasRequiredMain = 1;␊
    	main$1 = require$$0.dep;␊
    	return main$1;␊
    }␊
    ␊
    var mainExports = requireMain();␊
    var main = /*@__PURE__*/getDefaultExportFromCjs(mainExports);␊
    ␊
    module.exports = main;␊
    `

> Snapshot 2

    `'use strict';␊
    ␊
    function getDefaultExportFromCjs (x) {␊
    	return x && x.__esModule && Object.prototype.hasOwnProperty.call(x, 'default') ? x['default'] : x;␊
    }␊
    ␊
    var dep = {};␊
    ␊
    var hasRequiredDep;␊
    ␊
    function requireDep () {␊
    	if (hasRequiredDep) return dep;␊
    	hasRequiredDep = 1;␊
    	dep.dep = 'cjs';␊
    	return dep;␊
    }␊
    ␊
    var main$1;␊
    var hasRequiredMain;␊
    ␊
    function requireMain () {␊
    	if (hasRequiredMain) return main$1;␊
    	hasRequiredMain = 1;␊
    	main$1 = requireDep().dep;␊
    	return main$1;␊
    }␊
    ␊
    var mainExports = requireMain();␊
    var main = /*@__PURE__*/getDefaultExportFromCjs(mainExports);␊
    ␊
    module.exports = main;␊
    `

> Snapshot 3

    `'use strict';␊
    ␊
    function getDefaultExportFromCjs (x) {␊
    	return x && x.__esModule && Object.prototype.hasOwnProperty.call(x, 'default') ? x['default'] : x;␊
    }␊
    ␊
    var dep = {};␊
    ␊
    var hasRequiredDep;␊
    ␊
    function requireDep () {␊
    	if (hasRequiredDep) return dep;␊
    	hasRequiredDep = 1;␊
    	dep.dep = 'cjs'; dep.dep += requireDep().dep;␊
    	return dep;␊
    }␊
    ␊
    var main$1;␊
    var hasRequiredMain;␊
    ␊
    function requireMain () {␊
    	if (hasRequiredMain) return main$1;␊
    	hasRequiredMain = 1;␊
    	main$1 = requireDep().dep;␊
    	return main$1;␊
    }␊
    ␊
    var mainExports = requireMain();␊
    var main = /*@__PURE__*/getDefaultExportFromCjs(mainExports);␊
    ␊
    module.exports = main;␊
    `

## handles when a required dependency of a mixed ES module changes type

> Snapshot 1

    `'use strict';␊
    ␊
    function getAugmentedNamespace(n) {␊
      if (Object.prototype.hasOwnProperty.call(n, '__esModule')) return n;␊
      var f = n.default;␊
    	if (typeof f == "function") {␊
    		var a = function a () {␊
    			var isInstance = false;␊
          try {␊
            isInstance = this instanceof a;␊
          } catch {}␊
    			if (isInstance) {␊
            return Reflect.construct(f, arguments, this.constructor);␊
    			}␊
    			return f.apply(this, arguments);␊
    		};␊
    		a.prototype = f.prototype;␊
      } else a = {};␊
      Object.defineProperty(a, '__esModule', {value: true});␊
    	Object.keys(n).forEach(function (k) {␊
    		var d = Object.getOwnPropertyDescriptor(n, k);␊
    		Object.defineProperty(a, k, d.get ? d : {␊
    			enumerable: true,␊
    			get: function () {␊
    				return n[k];␊
    			}␊
    		});␊
    	});␊
    	return a;␊
    }␊
    ␊
    const dep = 'esm';␊
    ␊
    var dep$1 = /*#__PURE__*/Object.freeze({␊
    	__proto__: null,␊
    	dep: dep␊
    });␊
    ␊
    var require$$0 = /*@__PURE__*/getAugmentedNamespace(dep$1);␊
    ␊
    var main = require$$0.dep;␊
    ␊
    module.exports = main;␊
    `

> Snapshot 2

    `'use strict';␊
    ␊
    var dep = {};␊
    ␊
    var hasRequiredDep;␊
    ␊
    function requireDep () {␊
    	if (hasRequiredDep) return dep;␊
    	hasRequiredDep = 1;␊
    	dep.dep = 'cjs';␊
    	return dep;␊
    }␊
    ␊
    var main = requireDep().dep;␊
    ␊
    module.exports = main;␊
    `

> Snapshot 3

    `'use strict';␊
    ␊
    var dep = {};␊
    ␊
    var hasRequiredDep;␊
    ␊
    function requireDep () {␊
    	if (hasRequiredDep) return dep;␊
    	hasRequiredDep = 1;␊
    	dep.dep = 'cjs'; dep.dep += requireDep().dep;␊
    	return dep;␊
    }␊
    ␊
    var main = requireDep().dep;␊
    ␊
    module.exports = main;␊
    `

## handles ESM cycles when using the cache

> Snapshot 1

    `'use strict';␊
    ␊
    console.log('dep');␊
    ␊
    console.log('main');␊
    `

## handles external dependencies when using the cache

> Snapshot 1

    `'use strict';␊
    ␊
    var require$$0 = require('external');␊
    ␊
    function getDefaultExportFromCjs (x) {␊
    	return x && x.__esModule && Object.prototype.hasOwnProperty.call(x, 'default') ? x['default'] : x;␊
    }␊
    ␊
    var second$1;␊
    var hasRequiredSecond;␊
    ␊
    function requireSecond () {␊
    	if (hasRequiredSecond) return second$1;␊
    	hasRequiredSecond = 1;␊
    	second$1 = require$$0.second;␊
    	return second$1;␊
    }␊
    ␊
    var secondExports = requireSecond();␊
    var second = /*@__PURE__*/getDefaultExportFromCjs(secondExports);␊
    ␊
    var main = require$$0.first + second;␊
    ␊
    module.exports = main;␊
    `
