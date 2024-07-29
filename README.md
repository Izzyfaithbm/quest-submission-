# Quest Submissions

## Chapter 1 Day 1 

Answers to beginner Cadence course! :)

1. Blockchain is somewhere you can store info, view data, and interact with. The best part is there's no owner! So anyone can do anything (to a certain extent).

2. Smart Contracts are programs that people code to interact with others in the Blockchain. 

3. A transaction changes the data in a smart contract, whereas a script is used to view the contract.

## Chapter 1 Day 2 

My answers! :D

1. Safety/Security, Clarity, Approachability, Developer Experience, Resource Oriented Programming

2. Safety/Security is super useful to the users. Without it, others can hack into it and lots of bad things would happen.
   Clarity is useful to the users because if the person who developed the Smart Contract has bad intentions, it can easily be found within the code. Without clarity, the    code would be too difficult for users (who don't understand Cadence) to read and could possibly agree to a "malicious" contract.
   Approachability is good for developers. People who have coded before and want to learn Cadence will learn with more ease because of it's familiarity.
   Developer Experience is, obviously, useful to developers. It will motivate them to code and help them through confusing errors. 

## Chapter 2 Day 1

MY ANSWERS/CODE :)!

```cadence
pub contract JacobTucker {
  pub let is: String

    init() {
        self.is = "the best"
    }

}
```
![2022-09-07](https://user-images.githubusercontent.com/70292894/188973876-a96dcce8-b4e2-43b1-99fb-d47489bcaa5c.png)

## Chapter 2 Day 2

1. A script is only meant to be used to view data in a smart contract, therefore we wouldn't be able to use changeGreeting because only a trasaction can change data.

2. The AuthAccount type acceses the data in your account.

3. The prepare phase acceses info/data on your account, whereas the execute phase changes data on the blockchain. 

4. ![2022-09-09 (1)](https://user-images.githubusercontent.com/70292894/189458909-be5e1fe3-63ed-4dc5-9a62-70ea4495cb2b.png)

![2022-09-09 (2)](https://user-images.githubusercontent.com/70292894/189458923-0f50e02e-3a13-478f-803f-e1faf83c9463.png)

![2022-09-09](https://user-images.githubusercontent.com/70292894/189458940-2e05abb8-99a8-4b5b-a081-648d7f96dc1f.png)

## Chapter 2 Day 3
1. 
```cadence
var people: [String] = ["Mom", "Dad", "Me"]
log(people[0]) 
log(people[1]) 
log(people[2])
```

2.
```cadence
var names: {String: UInt64} = {"Facebook": 0, "Instagram": 1, "Twitter": 0, "YouTube": 2, "Reddit": 0, "LinkedIn": 0}
```
3.
The force-unwrap operator will unwrap an optional type and ask if it's nil or not. If it is, the entire program will abort. If it isn't, it will remove the optional type. Example:

```cadence
var good: Int? = 1
var unwrapGood: Int = good! // safe :)

var bad: Int? = nil
var unwrapBad: Int = bad! // ABORT! ABORT!
```
4.
The error message means that it is an optional, so it could be Int or nil. To fix the error, you have to add the force-unwrap operator, so make it "return thing[0x03]!"

## Chapter 2 Day 4 
my answers! :)

1.
```cadence
pub struct Apple {
    pub let taste: String
    pub let colour: String
    pub let amount: Int 
    pub let account: Address

    init(_taste: String, _colour: String, _amount: Int, _account: Address) {
        self.taste = _taste
        self.colour = _colour
        self.amount = _amount
        self.account = _account
    }
}
```

2.
```cadence
pub contract Authentication {

    pub var apples: {Address: Apple}
    
    pub struct Apple {
    pub let taste: String
    pub let colour: String
    pub let amount: Int 
    pub let account: Address

    init(_taste: String, _colour: String, _amount: Int, _account: Address) {
        self.taste = _taste
        self.colour = _colour
        self.amount = _amount
        self.account = _account
    }
}
    init() {
        self.apples = {}
    }

}
```
3.
```cadence
pub contract Authentication {

    pub var apples: {Address: Apple}
    
    pub struct Apple {
    pub let taste: String
    pub let colour: String
    pub let amount: Int 
    pub let account: Address

    init(_taste: String, _colour: String, _amount: Int, _account: Address) {
        self.taste = _taste
        self.colour = _colour
        self.amount = _amount
        self.account = _account
    }
}
    pub fun addApple(taste: String, colour: String, amount: Int, account: Address) {
        let newApple = Apple(_taste: taste, _colour: colour, _amount: amount, _account: account)
        self.apples[account] = newApple
    }

    init() {
        self.apples = {}
    }

}
```

4.
![2022-09-18](https://user-images.githubusercontent.com/70292894/190924884-319a6bf4-2074-442a-842a-a75926c55634.png)

5.
![2022-09-18 (2)](https://user-images.githubusercontent.com/70292894/190939177-49ee84c4-3937-46e1-b4c8-4c1d1db33a0f.png)

## Chapter 3 Day 1 

1. Unlike structs, resources cannot be copied, lost or created whenever you want.
2. If I wanted to transport something super important, like an NFT, a resource is perfect for making sure I don't lose it because of how secure it is. 
3. "create"
4. no
5. Jacob
6. - there is no @ symbol in front of the resource's type
   - resources cannot be copied, you would change = to <-
   - even after changing it to <-, it still wouldn't work because there is no "create" keyword before Jacob()
   - there should be a <- in between return and myJacob 
