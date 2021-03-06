# Strict mode

Angular CLI creates all new workspaces and projects with **strict mode** enabled.

Strict mode improves maintainability and helps you catch bugs ahead of time.
Additionally, strict mode applications are easier to statically analyze and can help the `ng update` command refactor code more safely and precisely when you are updating to future versions of Angular.

Specifically, strict mode does the following:

* Enables [`strict` mode in TypeScript](https://www.typescriptlang.org/tsconfig#strict), as well as other strictness flags recommended by the TypeScript team. Specifically, `forceConsistentCasingInFileNames`, `noImplicitReturns`,  `noFallthroughCasesInSwitch`.
* Turns on strict Angular compiler flags [`strictTemplates`](guide/angular-compiler-options#stricttemplates), [`strictInjectionParameters`](guide/angular-compiler-options#strictinjectionparameters) and [`strictInputAccessModifiers`](guide/template-typecheck#troubleshooting-template-errors).
* [Bundle size budgets](guide/build#configuring-size-budgets) have been reduced by ~75%.

You can apply these settings at the workspace and project level.

Using the basic `ng new` command to create a new workspace and application automatically uses strict mode, as in the following command:

<code-example language="sh" class="code-shell">

ng new [project-name]

</code-example>

To create a new application in the strict mode within an existing non-strict workspace, run the following command:

<code-example language="sh" class="code-shell">

ng generate application [project-name] --strict

</code-example>
