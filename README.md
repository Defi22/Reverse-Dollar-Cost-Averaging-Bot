# Reverse Dollar Cost Averaging Bot

## A smart contract on BSC which sells a fixed amount of tokens everyday



### Abstract

A smart contract (“SC”) which receives BEP20 tokens from various addresses (“users”), locks them and then starts selling a percent of the balance daily on Pancakeswap. The users cannot withdraw the tokens anymore but can withdraw the BUSD anytime. 

### Investor protection

The “Why”: The Bep20 holder target are the non-sophisticated traders and with this protocol we protect them from their own tendency to “buy high, sell low”. By locking the tokens in the smart contract the holders will allow the SC to sell small amounts of the tokens daily, no matter what the price is, and won’t have the temptation, nor the possibility, to sell during a crash. You may consider this as a reverse DCA (Dollar Cost Averaging) or a Programmed Profit Taking.  
Example

The SC receives the BEP20 token from 1000 different addresses and locks them. The users cannot withdraw them anymore, ever, if not in BUSD form after they’ve been sold. The senders can do this via a web interface and always see their balance.

On day 1, the SC starts selling 0.1% of the total initial BEP20 in balance on Pancakeswap for BUSD (note, it will take 1000 days to sell them all).
The SC now has a balance of both BEP20 and BUSD.

If possible, senders receive the BUSD with an internal gasless transaction daily. Alternatively, the senders can withdraw anytime the BUSD, paying the gas fees. They can’t withdraw the BEP20 which are going to be sold.



### Diagram 
Day 1 is the date when the SC starts selling the 0.1% daily.




### Examples of Flow

This is the flow from the point of view of the BEP20 token holder.
 Example 1: no hands approach

In this example the user does not withdraw the BUSD until the end.


User sends 100,000,000 BEP20 to the SC (worth $1969) on Day -100 (100 days before the SC starts selling).
The users sees “100,000,000 tokens staked. Sales will begin on [Day 1]”
On Day 1: “Sale started. Your balance is 99,900,000 staked tokens, $1.7 BUSD (withdraw BUSD here)”
On Day 30: “Your balance is 97,100,000 staked tokens, $69.10 BUSD (withdraw BUSD here)”
On Day 300: “Your balance is 70,000,000 staked tokens, $970.80 BUSD (withdraw BUSD here)”
On  Day 1000 (last):  “Your balance is 0 staked tokens (no tokens to withdraw), $3,503.61 BUSD (withdraw BUSD here)”


### Example 2: Withdrawing BUSD 

In this example the user withdraws BUSD from time to time.


User sends 100,000,000 BEP20 to the SC (worth $1969) on Day -100.
The users sees “100,000,000 tokens staked. Sales will begin on [Day 1]”
On Day 1: “Sale started. Your balance is 99,900,000 staked tokens, $1.7 BUSD (withdraw BUSD here)”
On Day 30: “Your balance is 97,100,000 staked tokens, $69.10 BUSD (withdraw BUSD here)”
User withdraws
On Day 300: “Your balance is 70,000,000 staked tokens, $901.70 BUSD (withdraw BUSD here)”
On  Day 1000 (last):  “Your balance is 0 staked tokens (no tokens to withdraw), $3,434.51 BUSD (withdraw BUSD here)”


Note:
The user can stake more tokens anytime.
If the deposit happens after Day 1 the sales start immediately.



## INTERFACE

Server hosted (no IPFS) simple yet pleasant interface on our own website, targeted at non sophisticated users.  
All happens in one page. 
Mobile friendly (most of our users use SafePal on mobile)
Deposit feature
Withdraw feature
Dashboard with major stats (for this wallet and general)

Wallets: connect to major wallets: Metamask, Wallet Connect, Portis, Binance etc…
Networks: BSC only.

Color scheme: We will provide it.

A good starting point would be the https://app.sushi.com/stake page, both in dark and light mode (light is default).


Stats:
Total tokens locked
Total tokens sold
Average price sold
Total BUSD withdrawn
Total BUSD available
BEP20 Token Price 
BEP20 Token 24h variation
BEP20  Token 7 days variation


## VARIOUS

it works with any standard BEP20 token
it works with any pair (not only BUSD)


## SMART CONTRACT

This is not a decentralised contract, we need to keep as much flexibility as possible in order to upgrade, bug fix and improve
The target users are new to crypto, we are educating them, and appreciate more safety than decentralisation, which they don’t understand. They trust us and they will hold us responsible if anything goes wrong.
In case of a bug/attack with loss of funds, we need to be able to stop the contract and transfers.
We would not be able to explain “it’s decentralised so we can’t do anything”.
The contract it’s conceived for our own use.

This needs to be declared clearly in the page.

We can:
Withdraw all tokens
Migrate liquidity to another contract
Stop the contract
Stop deposits
Stop withdrawals
Blacklist addresses
Change owner
Modify the pair (e.g. sell the tokens for BNB instead of BUSD)
Change Day 1 date
Change daily percent of tokens sold

In case some of these changes are better done by creating a new contract and migrate, we will do it. 

## HOW TO MAKE YOUR OFFER


Note: MAKE YOUR OFFER, THE VALUE WE DEPOSITED HERE IS JUST FOR REFERENCE. 
Tell us what you have done before in smart contract / frontend development (with links to your Github if available). 
Don’t apply if you are not confident you can do this. The contracts will hold significant amounts of money and need to be solid.
Comment/suggest improvements on these specifications
Ask questions if something is not clear.
Tell us how long it would take and how much it would cost (ranges are OK). The Gitcoin deposit we did is there just because it’s a necessary step and we had to put a number.
We are happy to create a new job with the agreed amount.


You can also contact us at defi@vaffatoken.com


