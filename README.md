# dmn-hierarchy
C8 evaluation of a DRD with sub decisions

When the Root DMN is invoked, with the inputs required for the sub-decision as well, the expectation is that the result of the sub-decision, in this example, the riskLevel (output from RiskLevel DMN) should be passed on as input to the Root DMN ( riskLevel defined as input expression in Car Loan granting DMN)


## Test Data

### Risk Level DMN -

For a Credit Score less than 80.0 the Risk Level is "high"

For a Credit Score greater than or equal to 80.0 and less than 95.0 the Risk Level is "medium"

For a Credit Score greater than or equal to 95.0 the Risk Level is "low"

### Car Loan Granting DMN -

For a Credit Score of 94.9 and Affordability “Affordable” the loan will be granted

For a Credit Score of 80 and Affordability “Marginal” the loan will be rejected

For all applications with a Credit Score < 80 the loan will be rejected

For a Credit Score >= 95.0 and “Marginal” the loan will be accepted
