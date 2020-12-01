# nice_readings

## javascript
<details><summary>(click to toggle)</summary>

in overall
- lit javascript https://developer.mozilla.org/fr/docs/Web/JavaScript/Une_r%C3%A9introduction_%C3%A0_JavaScript
- react vocab https://fr.reactjs.org/docs/glossary.html#single-page-application
  
on functions
- in overall https://developer.mozilla.org/fr/docs/Web/JavaScript/Une_r%C3%A9introduction_%C3%A0_JavaScript#Les_fonctions
- Immediately Invoked Function Expression https://developer.mozilla.org/fr/docs/Glossaire/IIFE
  
</details>
<br>

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
- create react app doc https://create-react-app.dev/
  - install dependencies https://create-react-app.dev/docs/installing-a-dependency

</details>
<br>

## to read list
<details><summary>(click to toggle)</summary>

https://reactfordesigners.com/
https://github.com/gilamran/fullstack-typescript
https://developer.mozilla.org/fr/docs/Web/API/File/Using_files_from_web_applications

</details>
