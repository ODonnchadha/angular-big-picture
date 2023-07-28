## Angular: The Big Picture by JOE EAMES

- INTRODUCTION:
    - What it is? Strengths? Weaknesses? Version 15. A framework.
        - Communicate with server.
        - Maintain state. Organize code & logic.
        - Ease display of data. Synchronize state as it changes.
        - Package application. Built-in tools to improve performance.
        1. Standards-based.
        2. Modern.
        3. Performant.
        - e.g.: Generate a new component.
            ```javascript
                ng new hello-angular
                cd hello-angular/
                ng g c about
                CREATE src/app/about.component.html
                CREATE src/app/about.component.spec.ts
                CREATE src/app/about.component.ts
                CREATE src/app/about.component.css
                UPDATE src/app/app.module.ts
                npm start
            ```
        - [Stackblitz](https://stackblitz.com/) Experiment. Online. (Can share URL with others.)
        - Major version every six months. And six months of active support.
        - Update your code using schematics.

- BENEFITS & FEATURES:
    - Reduction of cost. Standards compliance: ECMAScript. Modules. Internationalization and accessibility.
        - Performance. Open source. Requires TypeScript. (Types eliminate a given type of bug.) Signals library. (Optional.)
        - Backed by Google. (And they use it internally.) Uniformity. Enterprise-first. Popularity. Documentation.
    - Subjective: Framework. (Libraries.) Opinionated. (But not state management.) RxJS. Reactive data streams and asynchronous data.
        - Seperation of templates and logic.
    - Basic features: Progressive Web Apps. Lazy-loading. FOrms: Template-based and reactive. Reactivity: RxJS and signals.
        - Fully-featured router. Animations. Strictly-typed forms. CLI update.
    - Advanced features: Server-side rendering. Mobile-friendly. Full reactivity. ngUpgrade.

- ANGULAR ARCHITECTURE:
    1. Components: Foundation. Emerging of two pieces: Display (HTML. CSS.) + logic.
    2. Templates: The display of a component. Path or inline within the component decorator.
    3. Services: Code, or logic, that is not directly related to display. Reused logic. @Injectable({}) decorator.
    - Dependency injection: Components leveraging services.
    - Directives: Existing HTML tags new functionality. e.g.: Dragging functionality. Hover functionality.
    - Pipes: Formatting data for display. e.g.: ALL UPPERCASE.
    - Modules: "Grouping." e.g.: Inventory. Also: third-party code.
    - One-way data flow: Events and change detection. Parent component -> Children components.
    - Zone.js and change direction: Rerender display upon state change. e.g.: button click.
        - State change. FirstName changes. Cascading change. FullName changes. Re-render. 
            - System needs to under the cascade before re-render.
            - Zone creates a wrapper around state changes. -> notification -> Angular change detection.
    - Rendering targets: Not just a browser. Mobile. Server. Other desktops.
        - Changes the rendering engine. Browser-platform and browser-platform-dynamic.

- ANGULAR TOOLING & ECOSYSTEM:
    - CLI: JavaScript fatigue. New application. New component/service/pipe. etc. Servring up the application. Linting. Testing. Building.
        - Anount of time simply in order to start.
        - Module handling. Bundling. Minifying. TypeScript & ECMAScript transpilation. Browser shims. Zone.js. Testing. Monorepo. CSS.
    - Server-side rendering: Angular universal. 
        - Performance:Initial download size. Render time.
        - Search Engine Optimization.
        1. Full pre-render. Loaded on CDN
        2. Dynamic pre-render.
        3. Client-side switch: Download. Hidden div. Boots. Render. Replays events. Swap display.
    - Mobile/native frameworks: Mobile: Two tools: Ionic. NativeScript. Desktop: Electron.
    - Testing: 
        - Karma. Unit testing against multiple browsers. 
        - Protractor. E2E. (Termination of support.)
        - Alternatives: Jest. Cypress or Playwright.
        - Angular testing: TestBed. Async and fakeAsync. MockBackend.
    - AOT Compiler and Ivy: Ahead-of-time compiler. Ivy: Rendering engine.
    - Editors: TypeScript. (Intellisense. Type-related bugs.) Angular Language Service:
    - Ecosystem: VSCode. Stackblitz. HgRx. Nx. Angular Material.

- TIPS, TRICKS, & GOTCHAS:
    - Gotchas: 
        - TypeScript and Decorators: @Decorators(parameters...)
        - Custom Pipes. (Performance.) Pure versus impure. Impure pipes are complex.
        - Module API. And multiple modules: Feature areas. Lazy loading. Difficulties: ROuting. Importing.
        - Build. Complex.
        - Accessing the DOM. Wrapper. Hides complexity. Improves performance. Difficult to access the DOM.
        - RxJS: Promises versus observables. Self-subscribe. Or not. FOrgetting to subscripe. Or, subscribe multiple times.
            - Hot versus cold. Shared observables.
    - Tips and tricks:
        - Learn and use the CLI.
        - Learn and use TypeScript.
        - Learn and use NgRx.
        - Learn Webpack.
        - Follow the style guide.
        - Don't access the DOM.
        - Use signals.
        - Use lazy-loading.
        - Use VSCode.
        - Understand what you're sending down to the browser. Download bundle.
        - Use immutable or observeable data when appropriate.
        - Write effective unit and E2E tests.

- WHAT'S NEW IN ANGULAR:
    - Standalone components: Oficially released in version 15. (Module is still created.) Edge cases. Testing. { standalone: true }
    - Signals: 
        - Change detection:
            - e.g.: quantity. unitPrice. totalPrice. (totalPrice = quantity * unitPrice)
            - Angular Change Detection. Re-render everything? Or keep track of *old* values.
            - Ideal. *We* tell Angular what changes.
    - Misc. New Features: 
        - Stack trace improvements. Now more concise and useful. Display what is in our code.
        - Router guards: Functional router guards. Single line of code in route itself.

- PRESEENT & FUTURE:
    - Factors to consider: Enterprise? Typed backend? Templates seperate from code? Large backing company? 
        - Framework versus a set of libraries? Established track record? Popularity and momentum?
    - The future: Standalone components. Signals and reactivity. Server-side generation. Developer experience. CLI.
