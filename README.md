# IndexCertificate

IndexCertificate is a trading function which allows the issuer to setup up new index certificates. Potential buyers have the possibility to take part on the action of the certificate by using the platform which refers to the contract of the index certificate. 

#Smart contract 

The contract source code, IndexCertificate, is written in Solidity, Ethereum's language for constructing smart contracts.

#Smart contract structure

**string UnderlyingName :** Underlying Index Reference 

bool BuyerLong :  Long or short position of the Buyer  

uint IndexStrike :  Strike Price  

uint PayAmount :  Reward, if Strike is reached. Could also be a formula, etc.  

uint ContractPremium :  Premium to be paid by the buyer  

uint IndexValue :  Actual index value   

address Issuer :  address of the issuer, will be  determined and set automatically 

address Buyer :  address of the buyer,  will be determined and set automatically 
