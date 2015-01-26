# Maintainable and Scalable CSS

Contains a collection of (opinionated) best practice tips and advices on creating scalable and maintainable CSS for enterprise projects. Feel free to contribute by adding your thoughts and resource links.

## List of Resources

**Preprocessors**

- [LESS](lesscss.org)
- [SASS](sass-lang.com)
- [Stylus](http://learnboost.github.io/stylus/)

**Popular Style Guides**

- [SMACSS](https://smacss.com/)
- [OOCSS](http://oocss.org/)
- [BEM](http://bem.github.io/bem-method/html/all.en.html)

## Things to think about...

These are things that should go through your mind as you develop and make decisions on your architecture. Granted, some of these items may conflict with each other. Depending on the size and life of the project, some may be more or not at all relevant.

- How easy is it to navigate through the CSS project and find what you want?
- How easy is it to modify an element? Will it conflict with other elements? Is there too much ceremonies?
- Do you know which classes are used or not? How would you know if the class you are looking at is safe to delete or if it will cause hell to break loose?
- Is it clean and organized?
- Is the source easy to read?
- Are skin and layout classes distinguished?
- Is it themable? 
- Is it DRY?
- Is the cohesion between siblings or descendants strong and discoverable?
- Is it quick to develop with this method?
- How easy is it to reuse code?
- Is it easy for new members to discover elements and modify?
- Will new features be easy to add?
- How easy is it to create changes? What about global changes?

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

```
.Block {
    &__Element {}
    &--modifier {}
    &:state {}
    
    .SubElement {}
}
```

### Prefixes

Why use prefixes? It makes it easier to read through the source code and see which is which. It forces a strict sense of conscious difference between what a layout is versus what a component is.

- p-  page specific, usually applied on the body element;
- l-  layout like columns, wrappers, containers, etc...
- c-  for components
- u-  utility classes
- js- hooks for js; should never appear in css itself 
