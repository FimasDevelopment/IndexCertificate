# Ethereum Solidity based Index Certificate

An Index-Certificate is a financial instrument which allows you to invest in the market performance of an equity index. The blockchain technology allows issuers of certificates to setup up new index certificates on a platform in a very easy, cheap and fast manner. Potential buyers of a index certificate have the possibility to take part on the auction of the certificate by using the platform which refers to the contract of the index certificate.
The whole issuance process inclusively the processing can be significant eased by simply using the smart contracts of the block chain technology. All in all, many functional process steps could be avoided by using the mentioned bock chain functions. As a result, the market of the certificates could be revolutionized and profit margins would increase significantly


#Smart contract 

The contract source code, IndexCertificate, is written in Solidity, which is a programming language to setup smart contracts easily.

#Smart contract structure

**- string UnderlyingName :** Underlying Index Reference 

**- bool BuyerLong :**  Long or short position of the Buyer  

**- uint IndexStrike :**  Strike Price  

**- uint PayAmount :**  Reward, if Strike is reached. Could also be a formula, etc.  

**- uint ContractPremium :**  Premium to be paid by the buyer  

**- uint IndexValue :**  Actual index value   

**- address Issuer :**  address of the issuer, will be  determined and set automatically 

**- address Buyer :**  address of the buyer,  will be determined and set automatically 

**- function initiateCertificate(bool bLong, string uName, uint iStrike, uint cPremium, uint iValue, uint pAmount) :**
initialization of the Contract with the basis information. ContractPrice should be separate from the rest (constant and immutable
contract vs variable contract premium. Or other values declared private) **

**-  function buyCertificate(uint cPremium):** The Buyer enters into the contract, here by paying the Contract Premium.
The Issuer gets the Premium immediately.

**- function updatePrice(uint cPremium, uint iValue) :** only the issuer can update the contract premium and Index Value. Usually at the same time.

#Sample Case

Issuance of an index certificate for the DAX (Deutscher Aktienindex)

The issuer (bank xy) issues an index certificate with an endless lifespan. The mentioned index certificate represents the performance of the DAX over a period of time.  

**After the Contract has been created respectively issued the certificate have to be initialized with the following values by using the contract functions initialize contract.**

 - Index name or abbreviation **(uName) – DAX** 
 
 - Strike price on the issuance day **(iStrike) – 10302,46** 
 
 - Strike price on the validation day multiplied by exchange ratio **(cPremium) – 10302,46 * 0,01 = 103,0246** 
 
 - Total amount Amount **(Amount) – cValue multiplied by quantity – 103,0246 * 100 = 10302,46** 


**The potential buyer is using the contract function ‘buy contract’ to buy the index certificate. Therefore the following values have to be served.**

- Strike price on the validation day multiplied by exchange ratio **(cPremium) – 10302,46 * 0,01 = 103,0246**
- Total amount Amount **(Amount) – cValue multiplied by quantity 103,0246 * 100 = 10302,46** 

**Permanently or on daily basis the certificate has to be rated by serving the following values.** 

- Strike price on the validation day multiplied by exchange ratio **(cPremium) – 10400,46 * 0,01 = 104,0046**
- Total amount Amount **(Amount) – cPremium multiplied by quantity - 104,0046 * 100 = 10400,46**


#License information

Copyright (c) 2016 Fimas - Financial Market Solutions

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

