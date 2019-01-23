<h1> what is Ethereum?</h1>
<p>Ethereum is a next generation smart contract and decentralized application platform.Like bitcoin ethereum is a public blockchain network.</p>
<p>
Decentralized application properties are like<br>
1. Immutability<br>
2. privacy<br>
3. zero downtime<br>
    
</p>
<p>
There are five things in ethereum we need to know are<br>
1. smart contracts<br>
2. EVM<br>
3. solidity<br>
4. proof of work<br>
</p>
<h1>Smart contracts</h1>
<p>
it is just a bunch of code that manages the exchange of anything between two parties.In bitcoin we demand like or we can send one bitcoin from alice to bob but in ethereum by using smart contract we can send one ether from alice to bob if the date is 25th october or bobs current balance is 20 ethers.smart contracts selfexecute exactly as designed.
</p>
<h1>Ethereum virtual machine</h1>
<p>
this evm turns ethereum into a programmable blockchain keeping all the smart contracts running on time and coordinate them.
</p>
<h1>
Solidity
</h1>
<p>
Ethereum has its own programmable scripting language called solidity which is similar to javascript.it is used to write smartcontracts in ethereum.
</p>
<h1>
Ether
</h1>
<p>
Ether is the main internal crypto-fuel of Ethereum, and is used to pay transaction fees.
</p>
<h1>
Proof of work
</h1>
<p>
all miners are validate the transactions utill some one finish it.miners receive reward after they validate the transaction.after that is verify by all miners and that block will add to ethereum blockchain if 51 percent are agree.
</p>
<h1>
Principle to follow in ethereum
</h1>
<h5>
1.Simplicity
</h5>
<p>
The ethereum protocol should be as simple as possible and simple to understand even it cost or it takes more time.
</p>
<h5>
2.Universality
</h5>
<p>
Ethereum does not have features instead, Ethereum provides an internal Turing complete scripting language, which a programmer can use to construct any smart contract
</p>
<h5>
3.modularity
</h5>
<p>
It has to be comfortable to separable as possible as.
</p>
<h5>
4.Agility
</h5>
<p>
ability to move quickly and easily if any modifications are occure.
</p>
<h1>
Ethereum Accounts
</h1>
<p>
In ethereum the state contain some objects called accounts and each account contains four fields.<br>
1.The nonce, a counter used to make sure each transaction can only be processed once<br>
2.The account's current ether balance<br>
3.The account's contract code<br>
4.The account's storage<br>
There are two types of accounts those are externally owned accounts and contract accounts.
externally owned accounts controlled by private keys and contract accounts controlled by their contract code.<br>
In 
</p>
<h1>
Transactions
</h1>
<p>
transactions is used in ethereum to store and sent the message from externally owned account.<br>
Transaction includes.<br>
1.The recipient of the message<br>
2.A signature identifying the sender<br>
3.The amount of ether to transfer from the sender to the recipient<br>
4.An optional data field<br>
5.A STARTGAS value, representing the maximum number of computational steps the transaction execution is allowed to take<br>
6.A GASPRICE value, representing the fee the sender pays per computational step<br>
</p>
<h1>
Messages
</h1>
<p>
message is like a transaction but it is produced by a contract.a message contains<br>
1.The sender of the message<br>
2.The recipient of the message<br>
3.The amount of ether to transfer alongside the message<br>
4.An optional data field<br>
5.A STARTGAS value<br>

</p>
<h1>
Ethereum State Transition Function
</h1>
<p>
The transaction function is done like <br>
1.first check the transaction is valid,wellformed and nounce is matched with senders nounce.<br>
2.calculate the transaction fee based on the startgas and gasprice.By usging signature determine the senders address and subtract the transaction fee.if that much amount is not in senders accoung then return error.</br>
3.now send the transaction value to receiver account if receiver account not exist then creat it.if contract as receiver then run the contract code completly of until the execution runs out of gas.<br>
4.if sender account doesn't have that much amount  or the code execution ran out of gas then undo the all changes except payment of the fee and add the fees tominer's account.<br>
5.and refund the remaing converted ethers to senders account.<br> 
</p>
<h1>
Code Execution
</h1>
<p>
code in ethereum contracts is written in a low-level, stack-based bytecode language which referred as EVM code.code contains a sequence of byte where each byte represents the an operation.<br><br>
code execute infinitely and increment the program counter by one until the end of the code is executed successfully or an error occur or if it STOP or RETURN instruction is detected.<br><br>
every time the code will access the three types of space in the data store.those are<br>
1.The stack in which the last value pushed is pop   first.(last in first out).
2.Memory, an infinitely expandable byte array<br>
3.The contract's long-term storage, a key/value store. Unlike stack and memory, which reset after computation ends, storage persists for the long term<br><br>
4.The code can also access the value, sender and data of the incoming message, as well as block header data, and the code can also return a byte array of data as an output.
</p>
<h1>
Blockchain and Mining
</h1>
<p>
Both bitcoin blockchain and ethereum block chain are similar to eachother in many ways eventhough there are some extra functionalities in ethreum blockchain<br><br>
Bitcoin only contains a copy of the transaction list but in ethereum blocks contain a copy of both the transaction list and the most recent state.rather than these block also contain block number and difficulty.<br><br>
In Ethereum block validation done like<br>
1.Check if the previous block referenced exists and is valid.<br>
2.Check that the timestamp of the block is greater than that of the referenced previous block and less than 15 minutes into the future.<br>
3.Check that the block number, difficulty, transaction root, uncle root and gas limit (various low-level Ethereum-specific concepts) are valid.<br>
4.Check that the proof of work on the block is valid.<br>
5.Take the state at the end of the previous block.<br>
6.For every transaction set next state = APPLY(present state,present transaction). If any applications returns an error, or if the total gas consumed in the block up until this point exceeds the GASLIMIT, return an error.<br>
7.Check if the Merkle tree root of the state final state is equal to the final state root provided in the block header. If it is, the block is valid otherwise, it is not valid.<br>

</p>













