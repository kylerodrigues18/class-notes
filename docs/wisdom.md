# Programmer Wisdom

These are some things I've received from others that have had a profound effect on how I write code. Where I remember where I got them from, I'll give attribution. Where I haven't, just assume it wasn't me. ;)

## "Write the Code You Wish You Had"

-- Corey Haines 

```csharp

[HttpPost("/shoppingcart")]
public async Task<ActionResult> ProcessCart([FromBody] Cart request) 
{
// a bunch of validation and stuff here...

// then I have to verify the credit card number...
// "SPOT" - "Single Point of Truth"
var isCreditCardValid = _creditCardValidator.Validate(request.CardInfo);

}

```

## Avoid Premature Abstraction

Don't try to generalize a solution until you thoroughly understand the problem.

Don't go create helper classes, methods, etc. until you know what you need.

:::tip "Never type Private, Always Refactor To it"
- Another one from Corey Haines
::::


## JFHCI - "Just Hard Code It" 
This was advice for Ayende Rahein/Oren Eini 

Deploying software is easy. Don't prematurely build libraries, frameworks, configuration management gools, all that crap until you know you need it.



## Code Duplication Stuff

- "Single Point of Truth" - each piece of business knowledge should exist in exactly one place in an application (Kent Beck)
- "DRY" - "Don't Repeat Yourself"
- "Single Responsibility Principle" - "Each code module should have a single axis of change"
- "Instead of Dry write 'Moist' Code"


## Four Rules of simple Design
[Martin Fowler](https://martinfowler.com/bliki/BeckDesignRules.html)
Originated with Kent Beck
1. Passes the Tests
    - The code does the right thing
2. Reveals Intention
    - Is this legible? Can a trained programmer look at this and without documentation and understand it. Does it show what is intended?
3. No Duplication
4. Fewest Number of Elements

## Naming Things Kent Beck Style
When you are creating an abstraction (method, class, etc) and you aren't sure what to call it, that means you don't know what it is yet. Use something ridiculous for a name, like a fruit and change the name later when you figure it out.