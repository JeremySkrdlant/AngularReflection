# Modularity

The modularity in angular is different from react quite a bit. I am used to the props but the Input is interesting.  

## Source file html
```html
<app-custom [destinationVariable]="sourceVariable"></app-custom>
```

## Source ts file
```ts
    source:variableType;
```

## Destination ts file
```ts
  @Input() destination:variableType;
```

## Notes
The html is the same because you are putting the destination prop into the element.  I do like how you get to use Input to bind to a variable. It looks to be two way so a change in the child will update the parents variable. 
