# Forms Module, Looping, and Conditionals

It's been many years but I do remember a little working with Angular 1 back in the day.  The ng naming schema is comming back to me.  I do like how the ngModel is similar to the useEffect in react.    It is a little tricky remembering to import the FormsModule but it will probably become second nature after a bit.

## Forms Module  
Add code to app.module.ts
```angular
import { FormsModule } from '@angular/forms';

imports: [
  FormsModule
]
```

After you have that, you can add any variable you want to change it's state on with an form object like input with the following code.

```ts
  <input [(ngModel)]="variableName"] />
```

## Loops
You can create loops with the *ngFor.

```ts
    <div *ngFor="for car in cars">
       <p> You now have access to a {{car.element}} from the array creating a paragraph for each. </p>
    </div>
```

## Conditionals
You can show elements based on a *ngIf.

```ts
  <div *ngIf="variable == 5">
      This will only show if the variable is 5.
  </div>
```
## Conditional Classes
You can add a class to an element based on a condition.

```ts
  <div [class.neat]="project == 'neat'">
    This will show if the project variable is equal to neat.
  </div>
```

(click) for a click event, need to check other events.


# Project
The project I gave myself was a similar one I did with my students.  Create a textarea that when typed in shows the sha256 hash below it.  I also want to add a button that can store a previous value that can show in a list, when there is ever a match with an existing value, both modules will turn green.

## Issue 1
Installing the crypto-js library was a bit more difficult than it was in react. I ended up having to use the types like shown below.

```bash
npm install -D @types/crypto-js
```

## Success 1
After I got the library installed and working, it was easy to get the functionality I wanted.  I had a variable called currentString that was bound to a textarea.  The result area called a function that ran the hash function and returned a string.

```ts
currentString:string = "";

getHash(value:string):string{
  return crypto.SHA256(value).toString();
}
```
## Video
Here is a video of the rest of the progress.

[YouTube Video](https://youtu.be/8oZkahnEBOs)
