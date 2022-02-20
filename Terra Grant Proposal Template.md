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

Flappy Bird on Terra will bring back the legendary Flappy Bird mobile game, (with the [gaming rights IP](https://trademarks.justia.com/861/88/flappy-86188824.html) - to now be held in the Terra Treasury as an NFT), for a buildout in Web3 - combining NFT’s, play-to-earn [P2E] gaming mechanics and the addictive core loop of the original title as a casual gaming mobile dAPP.


### Overview

The original Flappy Bird, as released in 2013, is an arcade-style game in which the player controls the character (a bird), which moves persistently to the right. Players are tasked with navigating the bird through pairs of pipes that have equally sized gaps placed at random heights. Each successful pass through a pair of pipes would award the player one point. Colliding with a pipe or the ground ended the gameplay. 

Due to its addictive core loop, ease of access (mobile-no active internet required), and frustratingly difficult gameplay, Flappy became a cult classic, generating 50 million downloads by January 2014, making it one of the top free games on the Android and iOS app stores.
With our ownership of the Flappy Bird IP in hand, we aim to recapture the magic of the original Flappy Bird brand, while adding the best that Web 3.0 has to offer.

Flappy Bird on Terra will utilize Anchor’s API to leverage it’s yield earning components, transforming Flappy Bird into a Web 3.0 level progression game allowing for advancement, achievements, NFT’s and P2E mechanics (an asymmetric reward distribution based on player progress).

We have decided to relaunch the title now, having owned the Flappy Bird IP since 2018 but not finding the proper timing/ecosystem to execute on our vision until now. With so many clones and knockoffs of Flappy - in name and game-play, reintroduction of the original brand only became captivating with the P2E revolution taking place in Web 3.0.  Terra, through the Anchor protocol, is uniquely positioned to support the first casual P2E game in the space, differentiated from all the current role playing and NFT games currently saturating the space. We see the reintroduction of the Flappy Bird brand into Web 3.0 as a major win for casual/social gaming and a bridge between mobile (Web 2.0) and P2E (Web 3.0)


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
- Using Terra.js SDK and ANCHOR JS anchor gives 20% interest rate,  distribution of rewards 3%-1000% based on where they are in the world.  Asymmetrical reward system based on anchor.
- Minting of many X^Y (X power Y) number of birds where X is the number of skills like (health, attack type, defense type, etc…) and Y are the values.
- P2E UX needs to be easily to use and blockchain practically transparent. “My grandma can win crypto”. login, earn/buy/spend UST. This can be achieved by creating a session key the first time the user opens the app, and link this key to wallets and login accounts.
 
**GamePlay Insights**
- Infinite Levels that can be generated from 10 backgrounds and different spawning with procedural level generations.
- Internal NFT shop of birds and their upgrade (up to 3 times).
- If different updates are planned than will require a CDN service managed with the Addressable system.
 
 
**Challenges to overcome**
- List and minting of all NFTs (TBD how many/sale platform)
- Partnering, and Learning from Terra about their Anchor library to for p2e features
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

Help us locate your project in the Terra landscape and what problems it tries to solve by answering each of these questions:

- Where and how does your project fit into the ecosystem?
- Who is your target audience (parachain/dapp/wallet/UI developers, designers, your own user base, some dapp's userbase, yourself)?
- What need(s) does your project meet?
- Are there any other projects similar to yours in the Terra ecosystem?
    - If so, how is your project different?
    - If not, are there similar projects in related ecosystems?

## Team

### Team members

- Jonathan David: Co-Founder
- Chris Langbein: Co-Founder
- Starloop/TBD: CTO / Product Development 
   - Starloop Studios will handle initial development until we are out of beta, where upon an internal CTO and tech team will be hired.
- Elena Montija: Chief Creative Officer
- Will: Advisor
- Joe: Advisor
- Alex Ruthizer: Advisor


### Contact

- **Contact Name:** Jonathan David
- **Contact Email:** flappybirdterra@gmail.com
- **Website:** *Under Development*

### Legal Structure

- **Registered Address:** Address of your registered legal entity, if available. Please keep it in a single line.
- **Registered Legal Entity:** Name of your registered legal entity, if available.

### Team's experience

- Jonathan David is the co-owner of the Flappy Bird IP.  He has 7 years experience in mobile application development with Mobile Media Partners and Go Club Golf, helping to launch multiple top iOS and Google Play games including Apple’s first approved prize game WinSomething. Currently Jonathan is the co-founder and Managing Partner of BlockPoint Capital, a boutique cryptocurrency VC and trading fund, where he is focused on research, technology, trading system architecture, and advising token projects on liquidity and market dynamics.

- Chris Langbein is the co-owner of the Flappy Bird IP.  He has 12 years experience in mobile application development, most recently co-founding tech startup, Heard, a premier software and payments technology solution for restaurant and golf hospitality with golf legend Tiger Woods. Chris is also the co-founder and currently serves as CEO of two software development companies: Mobile Media Partners and Go Club Golf. Chris and his team have successfully launched several mobile apps that have garnered millions of downloads and reached top positions of the Apple App Store and Google Play Store charts. 
 
- Elena Montijo Capetillo is the lead designer for Doodle Jump (the hit iOS/Android game with over 250mm dowloads), a freelance illustrator, 2D animator, concept artist and game designer. For many years she has worked on children’s media, from editorial illustrations, childrens books, animated content for interactive and educational video and mobile games as well as supervising toy merchandise and product development. Her knowledge of Fine Arts combined with Digital and Mixed media along with her passion in traveling has allowed her a wider spectrum when it comes to creativity and innovative design concepts. 
 
- Alex has been working in the crypto space as an entrepreneur and investor since 2014.  He is a managing partner and founder of Blockpoint Capital, spending 2016-21 in Berlin overseeing the firm's European presence. Alex is focused on crypto investments, token project advisory and finance. Alex’s previous experience includes SpeechAgain, a revolutionary digital speech therapy app for stutterers, Strike Technologies, a trading infrastructure owner, and Affinity Capital Exchange, an exchange for securitized airline miles. Alex is a member of MetaCartel Ventures, one of the leading venture DAOs in the crypto space.  



### Team Code Repos

- [https://github.com/](https://github.com/)<your_organisation>
- [https://github.com/](https://github.com/)<your_organisation>/<project_1>
- [https://github.com/](https://github.com/)<your_organisation>/<project_2>

Please also provide the GitHub accounts of all team members. If they contain no activity, references to projects hosted elsewhere or live are also fine.

- [https://github.com/](https://github.com/)<team_member_1>
- [https://github.com/](https://github.com/)<team_member_2>

### Team LinkedIn Profiles (if available)

- [https://www.linkedin.com/](https://www.linkedin.com/)<person_1>
- [https://www.linkedin.com/](https://www.linkedin.com/)<person_2>

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

...

## Future Plans

Please include here

- how you intend to use, enhance, promote and support your project in the short term, and
- the team's long-term plans and intentions in relation to it.

## Additional Information

**How did you hear about the Grants Program?** Terra Website / Medium / Twitter / Element / Announcement by another team / personal recommendation / etc.

Here you can also add any additional information that you think is relevant to this application but isn't part of it already, such as:

- Work you have already done.
- Wheter there are any other teams who have already contributed (financially) to the project.
- Previous grants you may have applied for.
