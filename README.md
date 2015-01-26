# Maintainable and Scalable CSS

Contains a collection of (opinionated) tips and advices on creating scalable and maintainable CSS for enterprise projects. It is a continual work-in-progress and is waiting for your contributions.

## List of Resources

- https://smacss.com/
- http://oocss.org/
- http://bem.github.io/bem-method/html/all.en.html

## What does maintainable CSS and scalable CSS mean?

TODO: define scalability and maintainability

### Things to think about

Some of these items may conflict with each other. Also, depending on the size and life of the project, some may or may not even be relevant. 

- How easy is it to navigate through the files and find what you want?
- How easy is it to modify a property?
- Do you know which classes are used or not? Is this class safe to delete or will it cause hell to break loose?
- Is it clean and organized?
- Is the source code well structured and easy to read?
- Are skin and layout classes distinguished?
- Is it themable? 
- Is it DRY?
- Is the cohesion between siblings or descendants strong and discoverable?
- Is it quick to develop with this method?
- How easy is it to reuse code?
- Is it easy for new members to discover elements and modify?
- Will new features be easy to add?
- What about when new changes happen?

## BEM

BEM or block-element-modifier, is a method created by folks at Yandex, one of the leading internet companies in Russia. It provides better transparency and discoverability of what class does what to other developers without going into the CSS source. BEM started at 2007 and has since gain widespread momentum throughout the front-end ecosystem.

### Blocks

Are standable chunks of codes that should be modular and contain their own sets of elements. In other words they are somewhat like components or modules.

### Modifiers

Modifies the state of the block.

### Elements

TODO: description and examples

### Examples

### Naming Convention

### Key Takeaways

#### Pros

#### Cons

## OOCSS

## SMACSS

## Summary Key Points

- BEM
- SMACSS
- OOCSS
- Preprocessors
- Single-Class Components
- CSS size, though minimal is lower importance than maintainability

### Naming Convention

camelCase? Pascal? all lowercase? What really matters is having a strict convention and readability. Switching cases might lessen character types but they may have lower readability.

TODO: provide examples

### Example Folder Structure

/root
    /base
    /layout
    /components
    /views
    /vendors
    /themes

### Single-line or Multi-line CSS?

CSS should be written across multiple lines. Why? Diff.

It is easier to see what has changed, how many properties have changed with multi-line css than using just one full line. In addition, there is a much more reduced chances of merge conflicts because each property exists on its own line.

### Example CSS

.Block {
    &__Element {}
    &--modifier {}
    &:state {}
    
    .SubElement {}
}

### Prefixes

Why prefixes? It makes it easier to read through the source code and see which is which. It forces a strict sense of conscious difference between what a layout is versus what a component is.

p-  page specific, usually applied on the body element;
l-  layout like columns, wrappers, containers, etc...
c-  for components
u-  utility classes
js- hooks for js; should never appear in css itself 
