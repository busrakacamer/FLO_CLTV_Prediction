# CUSTOMER LIFETIME VALUE 

Customer lifetime value (CLV) is the total amount of money a customer is expected to spend with your business, or on your products, during the lifetime of an average business relationship. This is an important figure to know because it helps you make decisions about how much money to invest in acquiring new customers and retaining existing ones.

Knowing the CLV helps businesses develop strategies to acquire new customers and retain existing ones while maintaining profit margins.

![Ekran görüntüsü 2023-03-09 222125](https://user-images.githubusercontent.com/121626776/224132103-2ef38215-9dfe-4746-b399-9f5df5302a22.png)

## How is CLV calculated?

### CLV = (Customer Value / Churn Rate) * Profit Margin
### Customer Value = Average order value * Purchase frequency
### Average Order Value = Total price / Total transactions
### Purchase Frequency = Total transactions / Total number of customers
### Churn Rate = 1 - Retention rate

** Churn rate and profit rate come from the whole customers and are not personal.

Using this formula, the customer lifetime values of customers in the data sets are calculated. But this calculation refers to a single time period. It represents the time when the analysis is done.

If we want to predict the customer lifetime values of our customers in the future..

## Customer Lifetime Value Prediction 

Expected Number of Transactions * Expected Average Profit

BG/NBD Model * Gamma Gamma Submodel 

![Ekran görüntüsü 2023-03-09 222320](https://user-images.githubusercontent.com/121626776/224132604-b2f2d904-cb1d-4f4a-bd8d-8ae3b0ffa07b.png)

### BG/NBD MODEL 

The Beta-Geometric Negative Binomial Distribution (BG-NBD) model is an influential probabilistic model for describing customer behavior and for predicting customer lifetime value.

*How many transactions will be next week?

*How many transactions will be in the next 6 months?

*Which customers will do the most purchases in the next 3 weeks?

The BG/NBD model calculates the expected number of transactions. This model models 2 processes by using probability for predicting the expected number of transactions.

Transcation Process (buy) + Dropout Process (till you die)

### Transaction Process (Buy)

During the customer is alive, the number of will have made by the customer, will be distributed poison by transaction rate parameter.

While the customer is alive, they will continue to make purchases at their own transaction rate.

The transaction rates will differ for each client, and they will be distributed according to the gamma distribution with parameters r and α.

### Dropout Process (Till You Die)

Each customer has their own dropout rate by p probability.

The customer will be a dropout by p probability.

Dropout rates will change for each customer and they will be distributed beta (a,b) for the mass.


### Formula

E = Expected Value

x = The number of repeat sales for a customer. It should be greater than 1.

t(x) = The time is between a customer's first purchase and their last purchase. (Weekly)

T = It is the time since a customer's first purchase. The age of the customer. (Weekly)

r,α = comes from the gamma distribution (buy process). Transaction rate of the mass.

a,b = comes from the beta distribution (till you die process). The dropout rate of the mass.

Y(t) = expected number of transactions for each customer.


![Ekran görüntüsü 2023-03-09 215714](https://user-images.githubusercontent.com/121626776/224131310-c47094df-4cde-4d8e-88e2-41c35a9c1236.png)


### GAMMA GAMMA MODEL

 This model is used for forecasting how much average profit we can earn for each customers. It gives the expected average profit for each customers.
 
*The monetary value of a customer's transactions is randomly distributed around the average of the transaction values.

*The average transaction value may change between the customers over time, but not for a single customer.

*The average transaction value is gamma distributed among all customers.

### Formula

E = expected value

x = The number of repeat sales for a customer. It should be greater than 1.

mx = Monetary for each customer. Total Price/Total # of Transactions

M = expected value of transactions (expected average profit)

p,q,γ = comes from the gamma distribution

![image](https://user-images.githubusercontent.com/121626776/224340597-6abc6720-cf9f-4fc0-88b3-f5268f7d860c.png)

 
