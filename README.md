# Call_Center-Dashboard

## Dataset
The dataset comprises of 10 columns & 5000 rows. It pertains to a call center's operational metrics, capturing various aspects of interactions between agents and customers. Each record in the dataset represents a single call and includes the following attributes:

- Call Id: A unique identifier for each call.
- Agent: The identifier or name of the agent handling the call.
- Date: The date on which the call took place.
- Time: The time at which the call occurred.
- Topic: The subject or category of the call.
- Answered (Y/N): Indicates whether the call was answered by an agent (Y for Yes, N for No).
- Resolved: Indicates if the issue was resolved during the call (Yes/No).
- Speed of Answer in Seconds: The time taken (in seconds) for the agent to answer the call.
- AvgTalkDuration: The average duration (in seconds or minutes) the agent spent talking to the customer during the call.
- Satisfaction Rating: A numerical rating representing customer satisfaction with the call, often on a scale from 1 to 5 or 1 to 10.
  
- This dataset provides valuable insights into call center performance, agent efficiency, and customer satisfaction, enabling detailed analysis and improvement of service quality.

## Data Visualization with Dashboard
Tool Used - Microsoft Power BI 

1. Designed a Dashboard which displays the summarized data with meaningful insights.
   
![image](https://github.com/user-attachments/assets/183826f8-7e48-4119-8388-26ea28fa1c90)


2. DAX Measures
  - Total Callers
```
   Total Callers = COUNT(Sheet1[Call_Id])
```

  - Calls Answered
```
  No of answered = CALCULATE(COUNT(Sheet1[Answered (Y/N)]),FILTER(Sheet1,Sheet1[Answered (Y/N)]="Y"))
```

  - Resolved
```
  No of resolved = CALCULATE(COUNT(Sheet1[Resolved]),FILTER(Sheet1,Sheet1[Resolved]="Y"))
```

  - Target Satisfaction
```
  Target Satisfaction = 4.5
```


3. Conclusion drawn:
- Out of 5000 callers, agents answered 81.08% of the calls.
- Agents successfully resolved 72.92% of the concerns.
- The agents primarily addressed five topics: Contract-related issues, Streaming, Technical support, Payment-related inquiries, and Admin support.
- The average speed of answering calls was 67.52 seconds.
- Agent Jim handled the highest number of callers, while Agent Stewart had the fewest.
- The average satisfaction rating was 3.40, below the target of 4.5.
- The month with the highest number of calls answered was January.
- Agent Jim answered 536 calls and resolved 485 of them, the highest among all agents.

