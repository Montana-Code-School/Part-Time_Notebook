# Tuesday, April 6th

Today we will be discussing our “Todo” project, and moving into a conversation about responsive design, both with and without frameworks like Bootstrap.

* Standup
* Improv
* Go over JQuery Todo app
    * Discuss team workflow in Git
        * Feature branches
            * Create with `git branch branch_name`
            * Switch with `git checkout branch_name`
            * Once all changes are made, checkout the master branch, then `git merge branch_name`
        * Use issue tracking!
* Responsive Design
    * The practice of creating a website that can scale from a desktop form, to a mobile form.
        * Fixed vs Responsive, pixels vs percentages
        * CSS Media Queries
            * ```
<meta name="viewport" content="width=device-width, initial-scale=1”>
@media (max-width: 600px){ //only applies if the viewport width is less than 600px

}

@media (min-width: 600px){ //only applies if the viewport width is MORE than 600px

}
```
    * Bootstrap!
        * Simple and ubiquitous
        * Pros
            * Easy to get started.
            * A well structured framework, emphasizing a very practical grid system.
        * Cons
            * Very common to have to hack a bootstrap design
            * You can very easily spot a bootstrap design
* Exercises
    * Let’s make that Todo site of yours responsive.
        * Start with only media queries.
