# Object Oriented Programming

## The idea is to marry state and behavior
```vs
Dim myName as String
Set myName = "Jeff"

myName = UCase(myName)
```


```csharp
var myName = "Jeff";

myName = myName.ToUpper();
```
## To be an Object Oriented Language

The language must support the following 3 (or 4) things:

1. Encapsulation
    - Comes from the root word "Capsule"
    - We hide how we do things - this allows us to change it over time without impacting other code.
    - This is how we get "abstraction" - "concept"
2. Polymorphism
3. Inheritance
4. Runtime Type Inspection (not all agree with this)

:::info WHAT IS OOP BY ALAN KAY
OOP to me means only messaging, local retention and protection and

hiding of state-process, and extreme late-binding of all things. It

can be done in Smalltalk and in LISP. There are possibly other

systems in which this is possible, but I'm not aware of them. [Source](http://userpage.fu-berlin.de/~ram/pub/pub_jf47ht81Ht/doc_kay_oop_en)
:::

## Objects have:
### State
variables that the object "owns"

In .NET state is in class level variables, we use the term `Fields` for these.

### Behavior
code that can be invoked that has something to do with the data (state) owned by that object.

In .Net, the behavior is methods.

- Constructors

- Properties

- Events

### Properties in C#

Guidelines for deciding between properties and methods.

1. Properties *imply* no computation.
2. If you throw an exception on a property set or get, you are a jerk.
3. Once a property is set, then getting that property a bazillion times in a row should always return the same value.
    - so if I set `ah.Name = "Bob Smith"`, I should be able to read that over and over again and always get Bob Smith.
## Example
I have an object that represents a bank account.

### State
Bank Accounts have a current balance.

```csharp
public class BankAccount 
{
    private decimal _currentBalance = 0;

}
```
### Behaviors
We can make a deposit, and make a withdraw, and we can retreive our balance.

```csharp
public class BankAccount 
{
    private decimal _currentBalance = 0;

    public void Deposit(decimal amount) 
    {
        _currentBalance += amount;
    }

    public void Withdraw(decimal amount)
    {
        _currentBalance -= amount;
    }

    public decimal GetBalance()
    {
        return _currentBalance;
    }
}
```
### Varying Behavior

We need to make decisions, make code work one way under some situations, and other ways for other situations.

"if" statements, switches, and that sort of stuff.

#### Vary Behavior by Parameters

```csharp 
account.Deposit(20);
account.Deposit(100);
```

#### Vary Behavior based on the State of the object itself

```csharp
account.Withdraw(4999M);
account.Withdraw(2);
```

```csharp
account.Deposit(20);
account.Deposit(100);
```

```csharp
account.Type = AccountTypes.Gold;

account.Deposit(20);
account.Deposit(100);
```

#### Vary Behavior by Type

```csharp
var account = new BankAccount();
account.Deposit(100);
account.Deposit(100);
account.Deposit(100);
```

```csharp
var account = new GoldAccount();
account.Deposit(100);
account.Deposit(100);
account.Deposit(100);
```