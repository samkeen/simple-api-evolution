# simple-api-evolution

## Notes

### Stages of Project
1. Simple Lambda/APIG (code in CFn)
2. SAM + Dynamo
3. code pipeline
4. Demo issues with synchronis model on flawed deploy, how could this be fixed in sync model, issues with those strategies.
   Convert to asyn, demo same flawed deploy is auto recoverable
   
## Misc Notes

first build a service in the synchronous fashion
disadvantages 
- deploy fail can corrupt prod db
- errors pipe directly back to user

then add a work queue
Advantages
- errors can be detected on a prod deploy and then recovered from.
- If quickly resolved, customers are unaware (and unaffected) by these these error conditions

show the instrumentation disapline this takes.
run the same traffic (or demonstrate the same customer workflow) in both situations. Examine the result, and difference in customer experience.
