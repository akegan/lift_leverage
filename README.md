# Lift and Leverage in the Youth Risk Behavior Surveillance System

This is a quick project to look at co-occurance, lift, and leverage on a real dataset. It was inspired by Chapter 12 of [Data Science for Business](http://shop.oreilly.com/product/0636920028918.do) as a way to demonstrate some of the concepts for my analytics learning group.

## What are lift and leverage?

Lift and leverage are measures you can use to quantify the "unexpectedness" of combinations of items. They're used in the case were you have a users that have multiple items in baskets (either a real grocery basket or a hypothetical basket) and you want to get a feel for 

Lift is defined as **p(A,B)/(p(A)p(B))**, where p(A,B) is the probability of finding A and B in the same "basket" and p(A) and p(B) are the probabilities of finding A and B anywhere in the dataset respectively. Therefore a lift > 1 means that it's more likely to find A and B in a basket together than you'd expect than just by random chance.  

Leverage is a similar measure that also gives an idea of how unusually probable a given combination that uses subtraction instead of division. It's defined as **p(A,B) - p(A)p(B)** and gives an absolute percentage difference rather than a ratio. 

Lift and leverage do not fully characterize a dataset on their own, but as an unsupervised analysis they can provide some initial insight into your data. 

## What is the Youth Risk Behavior Surveillance System (YRBSS)?

The YRBSS is a survey given to US high school students every other year that ask them questions about various "risky" behaviors such as drug and alcohol use. The CDC makes this data public [online](https://www.cdc.gov/healthyyouth/data/yrbs/data.htm). The data is provided in an ASCII file format with accompanying pdf guide to column locations of questions. Q1-Q7 ask demographic information, and Q8-Q99 ask students to answer questions about their behaviors. The survey administrators have coded Q8-Q99 into binary yes/no answers that are given in QN8-QN99.

## Future direction

In the future it would be interesting to look at differences between ages, gender, and states and look into mild behaviors can be used to predict more risky behaviors (eg Marijuana use leading to injected drug use)


