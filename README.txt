tldr: 
Created a program where users can trade, sell and buy items. Once a trade is initiated, users can set up meetings and acknowledge that the meeting and trade happened. We have also added many new features that are noted in Features implemented for Phase 2.txt 

Requirements:
User Requirements: 
Users who participate in trades should be able to create an account, log in with a user name and password, maintain a list of items that they are willing to lend and a list of items that they wish to borrow. They should also be able to browse the inventory, looking for items to add to their wish list.

Users can lend items, borrow items, buy/sell items or trade items. However, they cannot borrow an item unless is it is part of a trade, or they have lent more items than they have borrowed. For example, everyone's first transaction must be lending, or trading.

After the transaction has occurred in real life, the user should be able to log in and confirm that the transaction has been completed. A transaction means a one-way, two-way trade or threeway trade. There is a limit on the number of transactions any one person can conduct in one week, and a limit on how many transactions can be incomplete before the account is frozen. An incomplete transaction is one where two users agree to a one-way or two-way trade, but one of them does not show up. Therefore, at least one person does not confirm to the program that the transaction occurred, because it did not.

A frozen account is one where you can log in and look for items, but you cannot arrange any transactions. A user who has been frozen can request that the administrative user unfreezes their account.

A user can request that an item be added to their own list of available items, but an administrative user must review the item and decide whether or not it should actually be added.

A user should be able to see the most recent three items that they traded in a one-way or two-way trade and their top three most frequent trading partners.

Administrative users should be able to log in with a username and a password in order to confirm that a user account should be frozen (even though the system identifies for them which users to freeze), add new items to user's lists of available items, or change any of the threshhold values (example: how many more times must you lend items before you can borrow).

In a previous paragraph, we said that a user must have lent (at least one) more item(s) than they have borrowed, in order to make a non-lending transaction. However, the administrative user should be able to change that to "at least two more items..." or "at least three..." etc.

The initial administrative user should be able to add subsequent administrative users to the system.

Inventories and Transactions
If a user wants to advertise that they have an item to trade, they should be able create a new item in the system with a name and description. It is not actually added to the system until an administrative user looks at it and confirms that it should be added. This is one way to prevent people from selling things they can't possibly own (example: the North Pole, a dinosaur, etc.) or otherwise entries that are not tangible objects (example: someone's self-respect, their loyalty, etc.).

Each transaction can be permanent or temporary. With a permanent transaction you give away an object that you do not expect to get back or you borrow an object that is now yours (referred to here as "permanently borrowing"). Either way, that item should be deleted from the wish list and list of available items of the users involved.

A temporary transaction has a time limit. This means that a second exchange is supposed to happen in the future. For Phase 1, you can assume this happens exactly one month after the original transaction, in the same location. However, this may change for Phase 2. You should design your program so this change is possible.

Meeting System
Once a transaction has been set up by one user on your system, the other user has to agree to the proposed trade. They also have to agree to a time and a place to meet. These two pieces of information should be entered by one of the users. The other can then confirm or edit. If they edit, then the original user can confirm or edit, and so on, until they both agree, up to a thresshold of 3 edits per user. If they both edit the time/place information three times without confirming, the system should print to the screen that their transaction has been cancelled.

Once the meeting has been set up, the associated transaction is open. To close it, both users have to confirm that the transaction took place, after the meeting was supposed to take place.

For a temporary transaction, the second meeting also has to be confirmed by both users, or else the transaction remains open, which counts towards both users potentially having their accounts frozen.


Assumptions we have made:
The only assumption we make is that users will never abandon the system in the middle of a trade.
They will always enter whether or not they showed up to the meeting, or if they got stood up.

There are also limitations for how much money each person can input into the system.


For your ease, we have created test users and test items in the system. Please keep in mind that logging in is case sensitive.
Below are the credentials:
Super Admin:
Username: Tina
Password: 123456

Users:
Username: Tina - Password: 123 - items they own: shoe, ebook, sock, book
Username: Mo - Password: 123 - items they own: pen
Username: A -  Password: 123 - items they own: phone

The current system thresholds are as follows:
lentMinusBorrowedThreshold = 1
meetingEditThreshold = 3
weeklyTransactionLimit = 7
incompleteTransactionLimit = 3

Please note that UML.pdf and UML.png are identical (aside from file type).
