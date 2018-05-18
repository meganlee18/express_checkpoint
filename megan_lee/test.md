# Node/Express Test

### Question 1

What is `module.exports` and why do we use it?

```text
This is necessary if user wants to use a function that is declared on another page on a new page. Having 'module.exports' declared tells the page to look up the function specified on another page and allows the function to be used.
```

### Question 2

Write one Express route for each of the four CRUD actions.

Then, make each route respond with a one-word string containing the RESTful action that would most likely be associated with this route.

```js
var express = require("express")
var app = express()

app.get('/', (req, res) => {
  res.send('READ')
})

app.post('/', function (req, res) {
  res.send('CREATE')
})

app.put('/', function (req, res) {
  res.send('UPDATE')
})

app.delete(',', function (req,res) {
  res.send('DELETE')
})

```

### Question 3

Describe the differences between Express and Rails as backend frameworks.

```text
1. Express is used for JavaScript while Rails is used for Ruby.
2. Rails is a bigger framework than Express
3. Rails is built with convention in mind e.g users have to follow conventions e.g creating and naming them in specific ways. Express is unopinionated e.g you can create your own files and name them whatever you want, however you want.
4. Ruby gems are global e.g installation takes place once. Express npm files are local which mean users have to download and install them each time they work on a project.
```

### Question 4

What do the following lines of code do?

```js
var bodyParser = require("body-parser")
app.use(bodyParser.json())
app.use(bodyParser.urlencoded({extended: true}))
```

```text
First, the project requires body-parser which is a NPM file which needs to be downloaded and installed for the project.

Second, the app looks and returns for middleware that parses JSON

Third, the app looks and returns middleware that parses urlencoded stuff/data??

```

### Question 5

For this exercise you will be creating an es6 BankAccount class.

It will have the following properties...
* `type` (e.g., "checking"), which should be determined by some input
* `balance`, which should start out as `0`

It should have the following methods...
* `withdraw`, which should decrease the balance by some input
* `deposit`, which should increase the balance by some input
* `showBalance`, which should print the balance in the bank to the console.

The `BankAccount` class has a `transactionHistory` property which keeps track of the withdrawals and deposits made to the account.
* Make sure to indicate whether the transaction increased or decreased the amount of money in the bank.

```text

var BankAccount = class {

  constructor() {
    this.type = type;
    this.balance = balance
    this.transactionHistory = transactionHistory
  }

  withdraw(num) {
    return this.balance - num
  }

  deposit(num) {
    return this.balance + num
  }

  showBalance() {
    return this.balance;
  }
}

```

Create an instance of the BankAccount class

```text

function BankAccount() {

  this.type = type;
  this.balance = balance;
  this.transactionHistory = transactionHistory;
  this.withdraw = function(num) {this.balance - num};
  this.deposit = function(num) {this.balance + num};
  this.showBalance = function(num) {this.balance};
}
  console.log(BankAccount.showBalance())

```
