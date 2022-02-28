# Terra Grant Proposal Template

### **FINAL DOCUMENT MUST BE SUBMITTED IN THE FORM OF A GITHUB REPO FORMATTED IN MARKDOWN**

> This document will be part of the terms and conditions of your agreement and therefore needs to contain all the required information about the project. Don't remove any of the mandatory parts presented in bold letters or as headlines! Lines starting with a > (such as this one) can be removed.See the Terra Grants Process on how to submit a proposal.
> 
- **Project Name:** Flappy Bird Development
- **Team Name:** Flappy Bird
- **Payment Address:** terra1k6ceterzd6anffvgq72zcv78v0e6tn4fzeptwd

> ⚠️ The combination of your GitHub account submitting the application and the payment address above will be your unique identifier during the program. Please keep them safe.
> 

## Project Overview

Flappy Bird on Terra will bring back the legendary Flappy Bird mobile game, (with the [gaming rights IP](https://trademarks.justia.com/861/88/flappy-86188824.html) - to now be stored as an NFT on the Terra blockchain). We are the sole owners of the Flappy Bird global trademark/inellectual property covering all gaming and digital rights usages - Now is the time bring Flappy Bird back to life for a buildout in Web3 - combining NFTs, play-to-earn [p2e] gaming mechanics and the addictive core loop of the original title - all as a casual gaming mobile dAPP. 


### Overview

The original Flappy Bird, as released in 2013, is an arcade-style game in which the player controls the character (a bird), which moves persistently to the right. Players are tasked with navigating the bird through pairs of pipes that have equally sized gaps placed at random heights. Each successful pass through a pair of pipes would award the player one point. Colliding with a pipe or the ground ended the gameplay. 

Due to its addictive core loop, ease of access (mobile and no active internet required during gameplay), and frustratingly difficult gameplay, Flappy became a cult classic, generating 50 million downloads by January 2014, making it one of the top free games on the Android and iOS app stores.
With our ownership of the Flappy Bird IP in hand, we aim to recapture the magic of the original Flappy Bird brand, while adding the best that Web 3.0 and p2e has to offer.

Flappy Bird on Terra will utilize Anchor’s API to leverage its yield earning components, transforming Flappy Bird into a Web 3.0 level progression game allowing for advancement, achievements, NFTs, player staking and p2e mechanics.

We have decided to relaunch the title now, having owned the Flappy Bird IP since 2018 but not finding the proper timing/ecosystem to execute on our vision until now. With so many clones and knockoffs of Flappy - in name and game-play, reintroduction of the original brand only became captivating with the p2e revolution taking place in Web 3.0.  Terra, through the Anchor protocol, is uniquely positioned to support the first casual p2e game in the space, differentiated from all the current role playing and NFT games currently saturating the space. We see the reintroduction of the Flappy Bird brand into Web 3.0 as a major win for casual/social gaming and a bridge between mobile (Web 2.0) and p2e (Web 3.0).

With this in mind our intention is to launch a Flappy Bird token on the Terra blockchain which will accrue value from game usage, community growth and NFT ecosystem. A native Flappy Bird token also positions the brand to extend into further Web 3.0 utility, such as an entire Flappy Bird metaverse. The tokenomics model is not as of yet finalized but will be created in collaboration with the Terra team.


### Project Details
We will be partnering with the gaming development studio StarLoop Studios, which has been vetted by members of the Terra team for the initial build out. Their TDD for flappy is as follows:

*Flappy Bird TerraLuna TDD Overview*
 
**Main Technical Features:**
- Delivery Platform: WebGL
- The project will be made using Unity 2020.3.x LTS.
- Version Control: GIT
- Wallet and Blockchain:
    - TerraStation to handles UST
    - Terra.js SDK and Anchor JS
- AzurePlayfab remote Leaderboards
- Optional CDN and Addressables Systems
- Security: Login System and Server Side logic on Azure Playfab and firewalls configurations to improve security.
- Cinemachine will be used for camera controls.
- Text Mesh Pro will be used for Text Rendering.
- DoTween: procedural animations
 
**NFT and Reward System**
- Using Terra.js SDK and ANCHOR JS anchor gives 20% interest rate which will flow through gameplay.
- Minting of many X^Y (X power Y) number of birds where X is the number of skills like (health, attack type, defense type, etc…) and Y are the values.
- p2e UX needs to be easily to use and blockchain practically transparent. “My grandma can win crypto”. login, earn/buy/spend UST. This can be achieved by creating a session key the first time the user opens the app, and link this key to wallets and login accounts.
 
**GamePlay Insights**
- Infinite Levels that can be generated from 10 backgrounds and different spawning with procedural level generations.
- Internal NFT shop of birds and their upgrade (up to 3 times).
- If different updates are planned than will require a CDN service managed with the Addressable system.
 
 
**Challenges to overcome**
- List and minting of all NFTs (TBD how many/sale platform)
- Partnering, and Learning from Terra about their Anchor library to for p2e features
- Creating a tokenomic model that is fair and accrues value for Flappy Bird players and Flappy token and Luna token holders.
- The connection with Wallet system (Less Friction)
    - https://medium.com/@cryptonumerist/how-to-acquire-the-base-stablecoin-of-terra-luna-buying-terrausd-ust-for-beginners-in-the-u-s-120923f143e
    - https://www.youtube.com/watch?v=4gnFM1CFbOk
 
 
*Code Standards and Guidelines [Internal]*
 
 
**Variables**

As a rule of thumb, every variable should be PRIVATE, unless there’s a good reason for a variable to be public. If you only need this variable to be shown in the Unity inspector, use the [SerializeField] attribute instead of making it public.
 
All variable names should be as descriptive as possible. Avoid using contractions. E.g. prefer writing “distance” over “dst”.
 
Variable names should use “camelCase”. E.g.: nameOfVariable.
 
Properties should use “PascalCase”. E.g.: NameOfProperty
 
Constants should be written in all caps: E.g.: NAMEOFCONSTANT
 
Parameter names should usually have different names than class member variables, but in case it might end up being less descriptive to change the parameter name, it can have a “_” before it. E.g.: _nameOfParameter
 

 
**Methods**

Just like variables, all methods should be PRIVATE unless it needs to be accessed by another class.
 
Public methods should always contain a “Summary” explaining what the method does.
 
 
Method names should be as descriptive as possible and usually have a verb in the name.
 
Method names should always use “PascalCase”. E.g.: NameOfMethod(parameter)
 
Curly brackets should be positioned on the next line following the parameters of the method: E.g.:
private void NameOfMethod(parameter)
{
              	\\Do something
}
 
When doing multiple method calls, try to spread the call into multiple lines. E.g:
someVariable.DoSomething()
              	.DoSomethingElse()
              	.DoOneMoreThing();
 
 
**Events & delegates**

Event names should follow the same rules of the variable names.
 
When using C# events, avoid using “Action” and “Func” and use “EventHandler<EventArgs>” instead, as that can help with possible future changes in the event parameters.
 
Use Actions and Funcs only when passing lambdas as parameters.
 
 
**Branching Policy**
    
The version control policy used will follow the “Git Flow” workflow.
 
Summarizing:
- The “Main/Master” branch is used for deployments ONLY, and each deployed version should be tagged with a version number. The version tag should be “vMajor.Minor.Fix”
- A “Hotfix” branch should be created for fixing and other changes that were overlooked, and should be merged to both the “Main” and “Develop” branches. Hotfixes branches should be named “hotfix/name-of-fix”
- A “Release” branch should be created for each “Release Candidate” (a version of the game that is ready for deployment, but still needs testing). Release branches should be merged to both “Main” and “Develop” when finished, just like Hotfixes. Release branches should be named “release/name-of-release”
- The “Develop” branch is the main branch developers should be working on, although the only commits that should be made into this branch are merges. Instead, developers should use this branch to create new “Feature” branches
- A “Feature” branch should be created for each new feature that’s going to be added to the “Develop” branch. Feature branches should be named “feature/name-of-the-feature”
- Hotfixes, Releases and Features branches should be DELETED after being merged.
- Ideally, a Pull Request should be created before merging a branch, for Code Review.
- The only person merging features should be the project lead, after doing the Code Review.
 
**UI**
    
The game UI will be separated into 3 “main” canvas:
 
- A “menu” canvas, where the current screen will be shown (for example, the inventory & quest UIs fits here). Only one screen of this type can be active at any time (making it work like a state machine)
- An “overlay” canvas, for popups and other temporary things that should be rendered in front of the main screen
- A “hud” canvas, where UIs that are active at basically all times are placed (like the coin counter)
 
This is done more for organization purposes, but we also get the benefit of being more performant since Unity won’t have to redraw the entire UI every time something happens.
Each “main” canvas can have its own sub-canvases if necessary.
 
Sometimes the game will need to mix some 3D elements with the UI elements. To achieve this, the game will use 2 cameras: a “world” camera and a “UI” camera.
 
- The world camera will render the environments and other “world” objects.
- The UI camera will be placed far away from the world camera and should be treated like a World Canvas, although its “render mode” should be set to “Camera”, with the UI camera as the reference. This basically means the placement of UI elements should take advantage of the Z axis for “layering” the 3D elements.
 
 
**Game Data Sheets**

Certain objects and data of the game will need to be tweaked many times. For that, we need to achieve the following criteria:
 
- Data needs to be easy to edit and test
- Data needs to be updated on clients without the need of a new build of the project
 
To fulfill these criteria, this data needs to be downloaded from the server and, for that, the project will use a mix of certain standards:
 
- Localization texts and item preferences will be defined using a CSV
- Objects will be created using prefabs, and will use Unity’s built-in Addressable


### Ecosystem Fit

Flappy Bird will be the first p2e casual mobile game in the Terra ecosystem.  We are not so much trying to solve a problem, as we are trying to bring further utility and usage to UST, specifically through the Anchor protocol. 

Our target audience will initially be the crypto native demographic (those familiar with crypto, nft’s, defi, etc).  There will initially be friction in onboarding of users due to the need to create Terra wallets and accounts.  Our long term vision is to create a more frictionless experience, more similar to the mobile Web 2.0 experience, allowing us to onboard non-crypto natives into the Terra ecosystem. We see Flappy’s long-term upside as an on-ramp and marketing tool for Anchor and its neo-bank products, as its brand recognition will bring interest of new users as well as provide a test case for integrating casual gaming into the terra ecosystem.  

Our project helps bridge the gap between non-crypto natives and casual mobile gamers.  It’s no secret that currently, the majority of p2e games are intense role playing games, and their UI/UX is often best rendered on PC, and not necessarily mobile friendly.  Similar to the Washington Nationals deal helping to bring Terra mainstream through a traditional marketing approach, we see Flappy Bird as a bridge to traditional commerce/gaming by offering a legendary brand in an innovative game with new tools (NFT’s, p2e, and DeFi).

While Terra is focused on building p2e games, has partnered with Gamevil, and is building out their own gaming arm, Flappy Bird is a unique brand and new approach to the p2e gaming revolution - focused on casual mobile gaming. We are not aware, as of yet, of any other game in the Terra ecosystem focused on this approach, and of course, Flappy Bird itself is an iconic brand to bring to the Terra ecosystem.

A similar and well funded project, [Fancy Birds](https://www.fancybirds.io/) is currently under way in the crypto space, being built on Polygon. Some of their better known investors include the following: Kain Warwick from Synthetix, Stani Kulechov from Aave, Tyler Ward from Barnbridge, angel investor Santiago Santos (ex-ParaFi Capital) and 0xmaki from Sushi.  Their next round of financing looks to include Framework Ventures, Delphi Digital and a16z.  What Fancy Birds does not have, is the original Flappy Bird brand, or the yield engine that is Anchor protocol and UST behind it. We will differentiate on brand and DeFi technology.
 
A thank you to the Terra team for their efforts in providing initial technical assistance on integration between the front end Flappy Bird build specs and the backend integration to Anchor protocol.  

Below are the initial tech specs per Terra:

**Tech Integration Overview**
1.	Necessary SDKs & Contract spec overview
2.	Decisions to be made & Challenges to overcome

 **SDKs and Contract Spec**
- Msg execution to Terra blockchain: Terra.js
https://github.com/terra-money/terra.js 
 - Since there will be only interactions with the new set of contracts, Anchor.js won’t be necessary
- Contracts: CosmWasm (Rust) (CW721 for NFT tokens)

 **Contracts**

 *Anchor Earn contract (Already made)*
- All principle reward will be generated from Anchor Market contract with UST deposits.

**Reward Contract**
 
 Reward contract is responsible for keeping track of each user’s (character’s) level.
- Based on each user’s attributes (within the NFT), the share of reward distributed to each address will change.
- Each users info consists of:
  - User address (or NFT token address): To identify the character / user eligible for the reward
  - Reward rate (level of each character): a number used to calculate the ratio of reward distribution each user is receiving (for example, if reward rates for 3 users are 1, 2, and 3, each user will get 1/6, 2/6, 3/6 of the total reward generated)
    - Make the parameter of the multiplier into something that is adjustable through an ExecuteMsg with a specific Auth
- Operations
  - Update reward rate: When there is an in-game change on each character’s level, a transaction must be made to the blockchain to Reward Contract to update the reward rate (This is an operation only authorized by the game server)
  - Claim Reward: Burns aUST to claim UST from Anchor Market contract for a specific user.

**NFT Contract (CW721)**
 
NFT standard that is compatible with Terra blockchain. Can be used to represent an individual character within the game.
- Operations
  - Mint (create character): A new CW721 token is created when user creates a new character in-game
  - Burn (burnt when deleting or upgrading): Only authorized to burn by the user or the NFT Upgrade contract.
- Features: attributes are applied to CW721 contract. We can create these contracts to have key (Names of skills and features) and value (Value applies to each Key)

**NFT Upgrade Contract**
- Upgrade rules: Tied to their progress within the game
- Customizations: Attribute updates from Game server / contract (no impact to the yield) - Check if one purchase of an attribute can be applied to the next NFTs characters

Upgrade of NFT will occur in the following flow:

1.	User sends a transaction to upgrade an NFT token by burning what he owned previously
2.	A new NFT token with new set of attributes is minted based on a set of “rule” for the upgrade (For instance, a rule could be something like combination of two NFTs that results in upgrade in specific value within the attribute field)
- Operations
  - Upgrade: consists of two separate operations where
    - burn: burns the NFTs currently owned by the user
    - mint: mints a new NFT as a result of burning the previous one (new attributes)

**Other components**
- Terra Station Wallet: Once Terra Station allows the login to the Flappy game, users do not have to login every time they play the game (unless the game has been updated or renewed)
  - Try to make it so that blockchain doesn’t seem to be involved - Starloop might have an idea
- Game Server: Every time there is an interaction between the game and the blockchain, a transaction has to be sent from the game to the chain in order to update the new state (for instance, if the user levels up, a transaction must be sent to the chain to update the state of the NFT)
  - One reason for having a centralized game server in the middle is due to potential transaction manipulation: Only authorized keys must be able to sign transactions that record level ups.

**Decisions to be made and challenges to overcome**
1.	Where does the initial amount of UST to generate Anchor yield come from?
     1. By selling NFT (which accrues Yield)
     2. Allow users to use Anchor Earn (later on)
     3. Marketing Options to be considered for the first x number of users
2.	Transaction queue: Terra blockchain as a queue of transactions. If the number / total sum of sizes of transactions exceed the max limit of each block, it will be automatically scheduled to be executed in the blocks to come after. There is no mempool, thus paying more tx fee won’t execute any transaction before others.
 

## Team

### Team members

- Jonathan David: Co-Founder
- Chris Langbein: Co-Founder
- Starloop/TBD: CTO / Product Development 
   - Starloop Studios will handle initial development until we are out of beta, where upon an internal CTO and tech team will be hired.
- Elena Montijo: Chief Creative Officer
- Will: Advisor
- Joe: Advisor
- Alex Ruthizer: Advisor


### Contact

- **Contact Name:** Jonathan David
- **Contact Email:** jonathan@flappybirdterra.com
- **Website:** http://flappybirdterra.com/ *Under Development*

### Legal Structure

- **Registered Address:** Address of your registered legal entity, if available. Please keep it in a single line.
- **Registered Legal Entity:** Name of your registered legal entity, if available.

### Team's experience

- Jonathan David is the co-owner of the Flappy Bird IP.  He has 7 years experience in mobile application development with Mobile Media Partners and Go Club Golf, helping to launch multiple top iOS and Google Play games including Apple’s first approved prize game WinSomething. Currently Jonathan is the co-founder and Managing Partner of BlockPoint Capital, a boutique cryptocurrency VC and trading fund, where he is focused on research, technology, trading system architecture, and advising token projects on liquidity and market dynamics.

- Chris Langbein is the co-owner of the Flappy Bird IP.  He has 12 years experience in mobile application development, most recently co-founding tech startup, Heard, a premier software and payments technology solution for restaurant and golf hospitality with golf legend Tiger Woods. Chris is also the co-founder and currently serves as CEO of two software development companies: Mobile Media Partners and Go Club Golf. Chris and his team have successfully launched several mobile apps that have garnered millions of downloads and reached top positions of the Apple App Store and Google Play Store charts. 
 
- Elena Montijo Capetillo is the lead designer for Doodle Jump (the hit iOS/Android game with over 250mm dowloads), a freelance illustrator, 2D animator, concept artist and game designer. For many years she has worked on children’s media, from editorial illustrations, childrens books, animated content for interactive and educational video and mobile games as well as supervising toy merchandise and product development. Her knowledge of Fine Arts combined with Digital and Mixed media along with her passion in traveling has allowed her a wider spectrum when it comes to creativity and innovative design concepts. 
 
- Alex has been working in the crypto space as an entrepreneur and investor since 2014.  He is a managing partner and founder of Blockpoint Capital, spending 2016-21 in Berlin overseeing the firm's European presence. Alex is focused on crypto investments, token project advisory and finance. Alex’s previous experience includes SpeechAgain, a revolutionary digital speech therapy app for stutterers, Strike Technologies, a trading infrastructure owner, and Affinity Capital Exchange, an exchange for securitized airline miles. Alex is a member of MetaCartel Ventures, one of the leading venture DAOs in the crypto space.  



### Team Code Repos

- Next Frontier Labs
  - [Rock Paper Scissors](https://github.com/pun777chy/Rock-Paper-Scissors)
  - [Car Jam Puzzle](https://github.com/nextfrontierlabs/CarJamPuzzle)
  - [Karate Fighter Zombie](https://github.com/nextfrontierlabs/KarateFighterZombie)

Please also provide the GitHub accounts of all team members. If they contain no activity, references to projects hosted elsewhere or live are also fine.

- [Elena Montijo](http://www.elenamontijo.com/)
- Chris Langbein
  - [Mobile Media Partners](https://www.mobilemediaco.com/)
  - [Go Club](https://goclubgolf.com/)
  - [Heard](https://www.tryheard.com/)
- Haris Ali Baig
  - [Next Frontier Labs](https://github.com/pun777chy)

### Team LinkedIn Profiles (if available)

- [Jonathan David](https://www.linkedin.com/in/jonathan-david-14139370/)
- [Chris Langbein](https://www.linkedin.com/in/chris-langbein-1990a145/)
- [Elena Montijo](https://www.linkedin.com/in/elena-montijo/)
- [Will]
- [Joe]
- [Alex Ruthizer](https://www.linkedin.com/in/alexruthizer/)
 

## Development Status

If you've already started implementing your project or it is part of a larger repository, please provide a link and a description of the code here. In any case, please provide some documentation on the research and other work you have conducted before applying. This could be:

- links to improvement proposals or RFP (requests for proposal),
- academic publications relevant to the problem,
- links to your research diary, blog posts, articles, forum discussions or open GitHub issues,
- references to conversations you might have had related to this project with anyone from Terra
- previous interface iterations, such as mock-ups and wireframes.

## Development Roadmap

This section should break the development roadmap down into milestones and deliverables. Since these will be part of the agreement, it helps to describe *the functionality we should expect in as much detail as possible*, plus how we can verify and test that functionality. Whenever milestones are delivered, we refer to this document to ensure that everything has been delivered as expected.

Below we provide an **example roadmap**. In the descriptions, it should be clear how your project is related to Terra. We *recommend* that the scope of the work can fit within a three-month period and that teams structure their roadmap as 1 milestone ≈ 1 month.

For each milestone,

- make sure to include a specification of your software. *Treat it as a contract*; the level of detail must be enough to later verify that the software meets the specification.
- include the amount of funding requested *per milestone*.
- include documentation (tutorials, API specifications, architecture diagrams, whatever is appropriate) in each milestone. This ensures that the code can be widely used by the community.
- provide a test suite, comprising unit and integration tests, along with a guide on how to set up and run them.
- commit to providing Dockerfiles for the delivery of your project.
- indicate milestone duration as well as number of full-time employees working on each milestone.
- **Deliverables 0a-0d are mandatory for all milestones**, and deliverable 0e at least for the last one. If you do not intend to deliver one of these, please state a reason in its specification (e.g. Milestone X is research oriented and as such there is no code to test).

> If any of your deliverables is based on somebody else's work, make sure you work and publish under the terms of the license of the respective project and that you highlight this fact in your milestone documentation and in the source code if applicable! Teams that submit others' work without attributing it will be immediately terminated.
> 

### Overview

- **Total Estimated Duration:** Duration of the whole project (e.g. 2 months)
- **Full-Time Equivalent (FTE):** Average number of full-time employees working on the project throughout its duration (see [Wikipedia](https://en.wikipedia.org/wiki/Full-time_equivalent), e.g. 2 FTE)
- **Total Costs:** Amount of payment in USD for the whole project. The total amount of funding *needs to be below $30k for initial grants* and $100k for follow-up grants. (e.g. 12,000 USD). This and the costs for each milestone need to be in USD; if the grant is paid out in Luna, the amount will be calculated according to the exchange rate at the time of payment.

### Milestone 1 Example — Implement Terra Modules

- **Estimated duration:** 1 month
- **FTE:** 2
- **Costs:** 8,000 USD

[Example Milestone Table](https://github.com/terramoney/terra-money-grants/blob/main/Untitled%20Database%20076bcbe63d9348558de4e6688af1d89e.csv)

### Milestone 2 Example — Additional features

- **Estimated Duration:** 1 month
- **FTE:** 1
- **Costs:** 4,000 USD

Flappy Bird Development Timeline

Use of proceeds - $30,000 to get Starloop started

Month 0 
Pre-production
Est Cost: $20,000
Source of funding: $30,000 Terra community grant

Month 1
Pre-Production 
Est Cost: $75,000
Source of funding: Terra community grant + follow on grant with Terra + misc Dev grants

Month 2-4
MVP Production
Est Cost: $350,000
Source of funding: Follow on grant with Terra + misc Dev grants+Dao investment+VC Investment

Month 5
Soft Launch and build in house team (GM, Devs, Producer)
Est Cost: $170,000
Source of funding: VC Investment

Month 6-12
Maintain Crypto version launch, build web 2.0/consumer version, build in house team (Devs, Marketing, Biz Dev)
Est Cost: $920,000
Source of funding: VC Investment and token launch

Month 12+
Launch  web 2.0/consumer version, continue to grow team
Estimated runway from remaining year 1 raise: $3 months
Source of continuing funding: VC investment


## Future Plans

- In game NFTs will be created prior to game launch.
- There will be a Flappy Bird token associated with the game, and those staking their pre-mined NFTs will be rewarded these Flappy Bird tokens.
- Depending on community support and interest prior to the game's beta launch, we will explore air dropping Flappy Bird tokens to the Terra community.
- Before determining tokenomics per the Flappy token as it relates to Anchor and Luna, we will be doing a deeper dive on the successes and failures of current popular p2e games such as Axie Infinity.
- The long term vision for Flappy Bird is to be a franchise title the likes of Mario Brother for Nintendo, but for Terra-Luna in Web 3.0, helping to drive UST adoption and Anchor Protocol usage.

## Additional Information

**How did you hear about the Grants Program?** Terra Website / Medium / Twitter / Element / Announcement by another team / personal recommendation / etc.

Here you can also add any additional information that you think is relevant to this application but isn't part of it already, such as:

- Work you have already done.
- Wheter there are any other teams who have already contributed (financially) to the project.
- Previous grants you may have applied for.
