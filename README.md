# LendLand - Where Risk is Opportunity

LendLand is a fictious P2P lending platform featuring an innovative way to solve the main limitations of existing P2P lending business models. The diverging priorities between the platform and risk-averse investors are addressed by offering subscription plans based on risk tolerance. Each subscprition plan is associated with a different automated trading strategy. Hence, once  your profile is set up, you just sit back and look at your worth grow! 

The code in this repository represents the Minimum Viable Product (MVP) of this novel business model. 

## Introduction
Peer-to-Peer (P2P) Lending is a platform business model where one user lends to the other. Traditionally, banks provide access to finance via bank loans. Because of conservative screening practices, banks grant loan requests only to creditworthy applicants. This behaviour aligns with the typically low risk tolerance of the majority of investors. The investors of a bank are depositors and equity holders. These investors gain a low return due to low risk and high credit quality. On the other hand, investors who are more risk-tolerant can achieve superior returns by directly lending to others. 

A P2P lending platform features three stakeholders:
1. investors (supply)
2. borrowers (demand)
3. platform (intermediary)

Demand comes from borrowers who would be rejected by banks due to low credit scores and a higher probability of default. The platform itself facilitates transactions between borrowers and investors. The typical revenue stream is based on the amount of transactions on the platform. The more the investors and borrowers, the higher the number of transactions. 

Compared to traditional banking, P2P lending suffers from adverse selection and information asymmetry. Once rejected by banks, less creditworthy borrowers turn to P2P lending platforms to look for finance. This phenomenon is referred to in economics as adverse selection. Moreover, due to lower barriers at the entrance and less disclosure requirements, P2P lending platforms promote information asymmetry between investors and loan orginators. 

Despite the potential for higher returns, lenders on P2P lending platforms still show risk-aversion. On the other hand, P2P lending platforms incentivise the presence of borrowers, even if risky, via lax screening procedures. Hence, there is a conflict between investors' preferences and business interests (Klein et. al, 2023). Moreover, it was found that wealthier investors tend to be more risk-averse on P2P lending platforms (Paravisini et al., 2017). Enhancing the match between supply and demand while strategically rethink the revenue stream could reconcile diverging priorities and create value for both investors and the platform.

LendLand's mission is to offer the opportunity of superior returns to the risk-averse investors.

## Risk-Adjusted Automated Portfolio Management for P2P Lending
A new P2P lending business model is proposed with the main innovation being an algorithm for risk-adjusted automated trading in the secondary market. At the moment of registration, the user indicates a level of risk tolerance which is mapped to a range of Probability of Default for the loans in the portfolio as follows:
- “low” → PD in range [0, 0.3)
- “medium” → PD in range [0.3, 0.6)
- “high” → PD in range [0.6, 1]

These thresholds indicate the extent to which the investor bears the risk of default on a loan in their portfolio. The algorithm predicts the probability of default of each loan in the portfolio every period. If at any time the threshold is exceeded, the loan is sold to another investor with a higher risk appetite.

## The Revenue Stream 
LendLand is a freemium business model. The customer journey starts with a Freemium account which features free registration and access. Users can register for free and access the basic features of the platform without any upfront charges. During registration, users complete a survey to self-select their risk tolerance, categorized into low, medium, or high risk. Investors manage their portfolios manually, buying and selling loans as they see fit. On top of that, a basic robo-advisory feature is available. This feature consists of a gentle reminder when a loan’s PD exceeds the user’s declared risk tolerance, and the recommendation to consider selling the loan. To unlock the full potential of robo-advisory and automated portfolio management, the platform offers monthly subscription plans. Subscription plans are tailored to the level of risk the investor is willing to bear. To prevent experienced investors from free-riding, thereby eroding subscription revenue, an investment cap is set for freemium accounts. For
example, given an investment cap of 5 loans/month, freemium users are allowed to trade 5 loans per month.

## How to execute
To reproduce this project locally, follow these steps:
- create the Data, Results, Models, and Plots folders in the parent directory of the cloned repository;
- download and save in the Data folder the Lending Club data from this link: https://www.kaggle.com/datasets/ethon0426/lending-club-20072020q1
- execute data cleaning, Macro variables, PD prediction, and Portfolio Management notebooks in this sequence.


## References
Klein, G., Shtudiner, Z., & Zwilling, M. (2023). Why do peer-to-peer (P2P) lending platforms fail? The gap
between P2P lenders' preferences and the platforms’ intentions. Electronic Commerce Research, 23:709–738.

OpenAI. (2024, May 24). DALL-E. From ChatGPT: https://chatgpt.com

Paravisini, D., Rappoport, V., & Ravina, E. (2017). Risk Aversion and Wealth: Evidence from Person-to-Person
Lending Portfolios. Management Science, Vol. 63, No. 2, pp. 279–297.
