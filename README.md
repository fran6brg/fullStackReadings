# nice_readings

## javascript
<details><summary>(click to toggle)</summary>

in overall
- lit javascript https://developer.mozilla.org/fr/docs/Web/JavaScript/Une_r%C3%A9introduction_%C3%A0_JavaScript
- react vocab https://fr.reactjs.org/docs/glossary.html#single-page-application

***tools to use js libraries in browser***
  - a brief review https://medium.com/the-node-js-collection/modern-javascript-explained-for-dinosaurs-f695e9747b70
  - 1) use a package manager to manage dependencies: npm
    - ```npm install x --save``` -> install x in node_modules + modify package.json
    - useful later when sharing a project with others
    - instead of sharing the node_modules folder (which can get very large), you only need to share the package.json
  - 2) use a module bundler to create a single, browser compatible, file from dependencies: webpack
    - ```$ npm install webpack webpack-cli --save-dev```
    - ```<script src="dist/main.js"></script>``` this avoid loading external scripts via global variables
    - live reloading ```npm install webpack-dev-server --save-dev``` + ```"server": "webpack-dev-server --open"```
  - 3) use a transpiler: babel
    - to transpile experimental/new features to browser compatible languages, since browsers are slow to update
  
on functions
- in overall https://developer.mozilla.org/fr/docs/Web/JavaScript/Une_r%C3%A9introduction_%C3%A0_JavaScript#Les_fonctions
- Immediately Invoked Function Expression https://developer.mozilla.org/fr/docs/Glossaire/IIFE

on use cases of looping through an array (functional programming) https://stackoverflow.com/questions/3010840/loop-through-an-array-in-javascript/6024310#6024310
- .forEach()
- .some()
- .map()
- .reduce()
- .filter()
- .sort()
- .find()

on the right way to write js
- standardjs https://standardjs.com/rules-fr.html 
- airbnb https://github.com/airbnb/javascript
- google https://google.github.io/styleguide/jsguide.html
- VSCode + ESLint + Prettier https://www.youtube.com/watch?v=lGCHjQl6XLw

on clean code
- ***"Your project should look like a forest, consisting of trees (module sections) and branches (groups of modules and module files)."***
- ***"Keeping logic in the right place is key to maintainability"***
- KISS
- DRY
- naming:
  - By reading the name of function or variable one should understand its purpose (getPost() {} - .isLoggedIn)
  - Don't add unnecessary context.
- functions:
  - a function should do one thing
  - function name should be a verb or a phrase fully exposing the intent behind it as well as the intent of the arguments.
  - use default arguments instead of conditionals
  - prefer multiple (1...4~5) parameters over single object parameters
  - don't use flags as parameters because they are telling you that the function is doing more than it should.
  - fail-fast approach: when writing a new function, return early and fail fast
  - function should not be larger than 20–25 lines. Smaller the function is better
- when using loops, prefer the functional programming way such as filter, map or reduce over traditional for loops
- don’t ever leave commented out code, otherwise known as “zombie code” in your codebase
- use better logger https://www.npmjs.com/package/winston
- use async/await of .then()
- module import order 3rd party packages ; reusable components ; utility functions ; submodules
- exports
  - use exports in Node.js
  - use destructuring
- conditionals:
  - use === instead of ==
  - avoid negative conditionals
  - whenever it's possible use polymorphism and inheritance instead.
- classes:
  - use method chaining.
- some nice libs
  - loglevel https://www.npmjs.com/package/loglevel
  - winston https://www.npmjs.com/package/winston
- try catch finally https://www.w3schools.com/jsref/jsref_try_catch.asp
- sources:
  - https://medium.com/javascript-in-plain-english/5-best-practices-for-writing-clean-javascript-be366adb2859
  - https://dev.to/deepaksisodiya/5-best-practices-for-clean-coding-in-javascript-26am
  - https://www.sitepoint.com/understanding-module-exports-exports-node-js/
  - https://devinduct.com/blogpost/22/javascript-clean-code-best-practices
  - https://blog.logrocket.com/12-tips-for-writing-clean-and-scalable-javascript-3ffe30abfe20/#:~:text=1.,do%20multiple%20things%20at%20once.
  
</details>

## node
<details><summary>(click to toggle)</summary>
- modules https://www.w3schools.com/nodejs/ref_modules.asp

</details>

## react
<details><summary>(click to toggle)</summary>

in overall
- getting started https://fr.reactjs.org/docs/getting-started.html
- courses https://fr.reactjs.org/community/courses.html

on components
- state and props
  - ***"The main responsibility of a Component is to translate raw data into rich HTML. With that in mind, the props and the state together constitute the raw data that the HTML output derives from."***
  - commonalities: objects, render update, deterministic
  - [see differences](https://fr.reactjs.org/docs/faq-state.html#what-is-the-difference-between-state-and-props)
  - state: initial value defined inside the comp. Optional, preferable without (+complexity and -predictability). Modified with setState()
  - props - properties: value received from parent component, immutable for "pure" component. Like function argument
  - async updates imply https://fr.reactjs.org/docs/state-and-lifecycle.html#state-updates-may-be-asynchronous
- lifecycle methods https://fr.reactjs.org/docs/state-and-lifecycle.html#adding-lifecycle-methods-to-a-class
  - 1) componentDidMount() "exécutée après que la sortie du composant a été injectée dans le DOM."
  - 2) componentWillUnmount() destruct the component
  - 3) componentDidUpdate()
  - nice schema https://projects.wojtekmaj.pl/react-lifecycle-methods-diagram/
- pass args to onEvent() attr https://fr.reactjs.org/docs/handling-events.html#passing-arguments-to-event-handlers
  - keys: "chaque élément à l’intérieur d’un appel à map() a besoin d’une clé"

on way to write components
- class
- function (Stateless (Functional) Components ou SFC) https://fr.reactjs.org/docs/hooks-state.html#hooks-and-function-components

on react x ajax requests
- todo inside componentDidMount(fetch("").then()...) https://fr.reactjs.org/docs/lifting-state-up.html#lessons-learned
- with hooks: const [error, setError] = useState(null); const [isLoaded, setIsLoaded] = useState(false); const [items, setItems] = useState([]);
- or without: this.state = { error: null, isLoaded: false, items: [] };
- fetch vs axios https://blog.logrocket.com/axios-or-fetch-api/
- env variables to store APIs keys https://medium.com/@trekinbami/using-environment-variables-in-react-6b0a99d83cf5

on forms
- multiple inputs https://fr.reactjs.org/docs/forms.html#handling-multiple-inputs
- formik https://formik.org/docs/overview
- hook form (seems > formik) https://react-hook-form.com/ | https://www.youtube.com/watch?v=bU_eq8qyjic

on hooks
- this section https://fr.reactjs.org/docs/hooks-overview.html
- useState: rather 1 than * vars in useState https://fr.reactjs.org/docs/hooks-faq.html#should-i-use-one-or-many-state-variables 
- useEffect: ...?
- *** les Hooks doivent être appelés au niveau racine des composants ***

web page design with components tree
- components tree design and hierarchy https://fr.reactjs.org/docs/thinking-in-react.html
- loop to display * components https://fr.reactjs.org/docs/lists-and-keys.html#rendering-multiple-components
- "délégation de contenu" https://fr.reactjs.org/docs/lifting-state-up.html#lessons-learned
- "spécialisation" https://fr.reactjs.org/docs/lifting-state-up.html#lessons-learned

on file organization
- by route or by type of file https://fr.reactjs.org/docs/faq-structure.html

on conventions
- DOM tag if downcase \<div \/> but \<Component \/> if uppercase
- Tout composant React doit agir comme une fonction pure vis-à-vis de ses props.
- Il ne doit y avoir qu’une seule « source de vérité » https://fr.reactjs.org/docs/lifting-state-up.html#lessons-learned

on vocabulary
- "faire remonter l’état" <=> déplacer dans le plus proche ancêtre commun

cheap metaphore
- "Si vous imaginez un arbre de composants comme une cascade de props, chaque état de composant est une source d’eau supplémentaire qui rejoint la cascade à un point quelconque, mais qui coule également vers le bas." https://fr.reactjs.org/docs/state-and-lifecycle.html#the-data-flows-down

tools
- react console
- create-react-app doc https://create-react-app.dev/
  - install dependencies https://create-react-app.dev/docs/installing-a-dependency
- nice boilerplate https://dev.to/nikhilkumaran/don-t-use-create-react-app-how-you-can-set-up-your-own-reactjs-boilerplate-43l0

</details>

## mern stack
<details><summary>(click to toggle)</summary>
- an overview https://github.com/accimeesterlin/mernapp_youtube
- nice packages
  - concurrently https://www.npmjs.com/package/concurrently
  - morgan https://www.npmjs.com/package/morgan
  
</details>

## vue
<details><summary>(click to toggle)</summary>

on vocabulary:
  - on syntax
    - rendu déclaratif
    - directives v-bind:title="", v-for:"n in ns", v:key, v-model="", v-if:
    - @eventToListen="methodName", v-on:click="..."
    - two way bindings
    - conditional :class="{ cssClassName: object.boolean }" @click="function(param)"
  - on logic
    - partie interface de l'app
    - partie logique de l'app
    - composition API vs option API

on workflow:
  - mount('#id')
 
</details>

## mongoDB
<details><summary>(click to toggle)</summary>
on relations between models
  - https://docs.mongodb.com/manual/tutorial/model-referenced-one-to-many-relationships-between-documents/
  
</details>

## eslint
<details><summary>(click to toggle)</summary>
- nice article https://www.synbioz.com/blog/tech/un-code-js-impeccable-grace-a-eslint
  
</details>

## to read list
<details><summary>(click to toggle)</summary>

cleared

</details>
