# Object Oriented Programming

```csharp
public class BankAccount {
    private decimal _currentBalance = 0;

    public void Depost(decimal amount) {
        _currentBalance += amount;
    }

    public void Withdraw(decimal amount) {
        _currentBalance -= amount;
    }

    public decimal GetBalance() {
        return _currentBalance;
    }
}
```

## Objects have State and Behavior
- State
    - Variables that the object "owns"
    - State is in class level variables, we use the term `Fields` for these
- Behavior
    - Code that manipulates the data (state)
    - Behavior can be methods, constructors, properties, events