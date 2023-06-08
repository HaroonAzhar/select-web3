# A guide on selecting web library/framework to develop frontend app.
There various option libraries and complete application solutions to build web3 project. In this guide we'll just focus on the ones that helpus to create client-side application. 

The primary idea behind our discusion will be the level abstraction each library offers and what will be the required input to enable interaction with a blockchain network. 

##Levels of abstraction:

* Level - 0: there isn't any library in this level. WOrking on this levl of abstraction menas to go out and build library that communicates with the blockchain. OUR result could something comprehensive like ethers.js or ssomething smaller too, depends upon our needs.

    *  Pros: Full control, what you implement, how you implement, what chains you support , what gateways , all upto you. 

    * Cons: requires http netwwork protcols and security best practices expertise.

    *  Cost of setting in up boilerplte to get started with interracting with blockchains : Months 

* level - 1 : The only 2 prominent option here are ethers.js and web3.js.. Even though web3.jss is build on top of ethers.js, it uses some utility functions from ethers.js but remain almost at the same level of abtraction. At this level of abstraction we just have mechanism to communicate with etherium based chains. Now you'll need to implement/define frontend library specific functionalities or utility functions for your project. In context of React specifically, it means creating hooks for different interactions/events, state handling logic, test suite etc. We can use ethers.js or web3.js to boost our development speed. Ethers.js is the  best option hands down on the  layer of abstraction .
 
    * Pros: 1- have providers for conecting etherium networks  2- almost full control as level 0 

    *Cons:  2- requires development of already available hooks out there and producing library specific quality solutions(e.g state management choice using react-query)

    *Cost of setting in up boilerplte to get started with interracting with blockchains : 1-4 weeks, basic wallet-auth feature will take 1-2 weeks.   

* level - 2 : There are few good options here. Top 3 options are wagmi , web3-react , useDapp. At this level of abstraction we just have mechanism to communicate with etherium based chains. Now you'll need to implement/define frontend library specific functionalities or utility functions for your project. In context of React specifically, it means creating hooks for different interactions/events, state handling logic, test suite etc. The best solution here is Wagmi with 1) most hooks + cache mechanism + persistence 2) flexbile support packages for multiple frontend frameworks 3) typescript and test suitess.

    * Pros:  1- ready to work with blockchain eth nodes. 2- simplified code. 

    * Cons:  1- size of project will need to be controlled (wagmi supports tree shaking) 2- restricted control : what connector we can use, supported chains, frontend library specific solution(e.g no vanilla js with web3-react)

    * Cost of setting in up boilerplte to get started with interracting with blockchains : 2 -3 days. 

* level - 2.5 : The  best solutions are based on-top of wagmi and have additional devEx bonuses for client side development. UI-Connect(based on top of wagmi) is the best option here with simple setup catered for using best modern practices and tools. Seprerate package for next.js with ability to make a backend-less server for complete sign-in flow. It has the most depth of utlity for development compared to something like web3-onboard which is good for connecting  and manging wallets but will become stale or redundant when we'd like to define behavior of client app on blockchain changes.
 
    * Pros:  1- modern and more refined solutions

    * Cons:  same as level 2 options 

    * Cost of setting in up boilerplte to get started with interracting with blockchains : 2 -3 days. 

* level 3: WEB3 appilication development SDKs and platforms. Have  prices and tiers. provids complete end-to-end development solution to spin up a swift web3 project with bare minimum code.  

    * Pros:  BLZING-LY fast development and extremely simplified.

    * Cons:  subscription for code and resources, requiress fiat.

    * Cost of setting in up boilerplte to get started with interracting with blockchains :  can spin up a full app(backend and frontend) in about 3 days

Recommnedation: use ConnectKIT from Level 2.5. 
