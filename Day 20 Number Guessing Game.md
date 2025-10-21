# Number guessing game in javscript

```jsx
const min = 1;
const max = 100;
const answer = Math.floor(Math.random() * (max - min +1))+min;
let guess;
let attempts  = 0;
let running = true;
while(running){
    guess= window.prompt(`guess  a number betweeen ${min} - ${max}`);
    guess = Number(guess);
    if(isNaN(guess)){
        window.alert("enter a valid number");
    }
    else if(guess < min|| guess > max){
        window.alert("please enter a valid number");
        
    }
    else{
        attempts++;
        if(guess < answer ){
            window.alert("too low try again")
        }
        else if(guess > answer) {
            window.alert("too high try again ");
            
            
        }
        else{
            window.alert(`you got the number ${answer} in ${attempts} attempts`);

             running= false;

        }

    }
}
```