DAPcoin-Spec
============

DAPcoin (Decentralized Applications and Protocols) Complete Specification
=================================

vs0.1 (Basic Version)

DavidJohnstonCEO (djohnston at gmail dot com)

# Summary

We claim that

(David Build these Claims)
* Will financially benefit the entire DistributedAppscoin user community, including those who don’t use the type III Decentralized Apps protocol layers.
* Will provide initial funds to hire developers to build upon software and ongoing funds to pay for maintenance of this software.
* Will richly reward early adopters of the type III Decentralized Apps protocol and tokens, in proportion to how successful it is.

# Assumptions

Our claims are built on the following assumptions:

* (David Build these Claims)
* 
* 
* 
* 
* 
* 

Note that all transfers of value are still stored in the normal bitcoin block chain via the Mastercoin protocol with higher layers of the protocol assigning additional meaning to some transactions.

# Document History

1. Version 0.1 released 11/23/2013 (Initial Document Offering)

Previous versions of this document can be found at:

# Operating on Top of the Mastercoin Design

The “DistributedAppscoin” protocol uses the Mastercoin Protocol to create a user currency identifer and will financially benefit the entire user community, including those who don’t use the type III Decentralized Apps protocol layers.

## The “DAP Address”

Initial distribution of DistributedAppscoin will essentially be a fundraiser to provide money to pay developers to write the software. The distribution is very simple, and will proceed as follows:

1. Anyone sending bitcoins to the Exodus Address before February 15th,2014 is recognized by the protocol as owning 100x that number of DistributedAppscoins. For instance, if I send 100 bitcoins to the Exodus Address before February 15th,2014 my bitcoin address owns 10,000 Mastercoins after August 31st. 
2. Early buyers get additional Mastercoins. In order to encourage adoption momentum, buyers will get an additional 10% bonus Mastercoins if they make their purchase a week before the deadline, 20% extra if they purchase two weeks early, and so on, including partial weeks. Thus, if I send 100 bitcoins to the exodus address 1.5 weeks before August 31st, the protocol recognizes my bitcoin address as owning 11,500 Mastercoins (10000 + 15% bonus).
3. Attempts to send funds to the Exodus Address on or after September 1st 2013 (as determined by bitcoin block chain records) will not be considered Mastercoin purchases. (**Update 9/8/2013: **Transactions sent before the deadline but not included in a block until after the deadline may be included. This is still under discussion at the time of this writing)


In the event that a purchase has multiple inputs, the input address contributing the most funds is recognized as owning the Mastercoins.

Note that anyone who purchases Mastercoins also receives the same number of “Test Mastercoins” which will be used for testing new features before they are available for use in the Mastercoin protocol.

Initially, the only valid Mastercoin transaction will be a “simple transfer” (defined later in this document), but the additional features described in this document will also become valid in the future (at specific pre-announced block milestones) once they are fully tested.

## Developer DAPcoins

For every 10 DAPcoins sold, an additional “Developer DAPcoins” will also be created, which will be awarded to the Exodus Address slowly over the following years. These delayed Mastercoins will ensure that we have plenty of motivation to increase the value of DAPcoin by completing the features desired by users. The reward will be structured so that we receive 50% of the reward by one year after the initial sale, 75% by a year later, 87.5% by a year later, and so on:

## Transferring DAPcoins

Say you want to transfer 1 Mastercoin to another address. Only 16 bytes are needed, which fits into a single data payment. The data stored is:

Note that the amount to transfer is multiplied by 100,000,000 before it is stored, which allows for Mastercoins to be sent with the same precision as bitcoins (eight decimal places). The reference payment (described earlier) determines the address receiving the Mastercoins.

Note that if the transfer comes from an address which has been marked as “Savings”, there is a time window in which the transfer can be undone. Otherwise Mastercoin transactions are not reversible.


## Selling DAPcoins for Bitcoins

Say you want to publish an offer to sell 1.5 Mastercoins for 1000 bitcoins. Doing this takes 33 bytes, which fits into two data payments:

1. Transaction type = 20 for currency trade offer for bitcoins (32-bit unsigned integer, 4 bytes)
2. Currency identifier for sale = 1 for Mastercoin (32-bit unsigned integer, 4 bytes)
3. Amount for sale = 150,000,000 (1.50000000 Mastercoins) (64-bit unsigned integer, 8 bytes, should not exceed the number owned, but if it does,  assume the user is selling all of them)
4. Amount of bitcoins desired = 100,000,000,000 (1000.00000000 bitcoins) (64-bit unsigned integer, 8 bytes)
5. Time limit = 10 (10 blocks in which to send payment after counter-party accepts these terms) (8-bit unsigned integer, 1 byte)
6. Minimum bitcoin transaction fee = 10,000,000 (require that the buyer pay a hefty 0.1 BTC transaction fee to the miner, discouraging fake offers) (64-bit unsigned integer, 8 bytes)


## Selling DAPcoins for Other Mastercoin-Derived Currencies

Say you want to publish an offer to sell 2.5 Mastercoins for 50 GoldCoins (coins which each represent one ounce of gold, derived from Mastercoins and described later in this document). For the sake of example, we'll assume that GoldCoins have currency identifier 3. Doing this takes 28 bytes, which fits into two data payments:

1. Transaction type = 21 for currency trade offer for another Mastercoin-derived currency (32-bit unsigned integer, 4 bytes)
2. Currency identifier for sale = 1 for Mastercoin (32-bit unsigned integer, 4 bytes)
3. Amount for sale = 250,000,000 (2.50000000 Mastercoins) (64-bit unsigned integer, 8 bytes, should not exceed the number owned, but if it does,  assume the user is selling all of them)
4. Currency identifier desired = 3 for GoldCoin (32-bit unsigned integer, 4 bytes)
5. Amount of GoldCoins desired = 5,000,000,000 (50.00000000 GoldCoins) (64-bit unsigned integer, 8 bytes)











