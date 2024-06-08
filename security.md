For Security Reasons we will summuray the n8n template code into text as follow:
**Workflow Summary:**
**Additional Processing:**
- **Schedule Trigger** (n8n-nodes-base.scheduleTrigger)
  Details:
    - **Notes**: ```plaintext
Run Every 15 minutes``` 
- **Sticky Note** (n8n-nodes-base.stickyNote)
  Details:
    - **Content**:
```plaintext
## USDT TRC20 Wallet Tracker
**This workflow** Is a basic concept of integrating your TRC20 wallet with N8N Nodes.
‌ ‌ ‌ ‌‌ ‌ ‌ ‌‌ ‌ ‌ ‌‌ ‌ ‌ ‌‌ ‌ ‌ ‌‌ ‌  ‌ ‌‌ ‌ ‌ ‌‌ ‌ ‌‌ ‌ ‌ ‌‌ ‌ ‌ ‌‌ ‌ ‌ ‌‌ ‌ ‌ ‌ ‌ ‌ ‌ ‌ ‌‌ ‌ ‌ ‌‌ ‌ ‌ ‌‌ ‌ ‌ ‌‌ ‌ ‌ ‌‌ ‌ ‌ ‌‌ ‌ ‌ ‌ ‌ ‌ ‌ ‌‌ ‌ ‌ ‌‌ ‌ ‌ ‌‌ ‌ ‌ ‌‌ ‌ ‌ ‌‌ ‌ ‌ ‌‌ ‌ ‌ ‌‌ ‌ ‌ ‌‌ ‌ ‌ ‌ ![Logo](https://static.tronscan.org/production/logo/usdtlogo.png) 

``` 
- **Edit Fields** (n8n-nodes-base.set)
  Details:
    - **Notes**: ```plaintext
Wallet Config``` 

**Data Fetching and Processing:**
- **TronScan API** (n8n-nodes-base.httpRequest)
  Details:
    - **Notes**: ```plaintext
Request Wallet Status``` 

**Additional Processing:**
- **Split Out** (n8n-nodes-base.splitOut)
  Details:
    - **Notes**: ```plaintext
Format response``` 
- **Filter** (n8n-nodes-base.filter)
  Details:
    - **Notes**: ```plaintext
Received in last 15m only``` 
- **Final Results** (n8n-nodes-base.set)
  Details:
    - **Notes**: ```plaintext
Keep only required fields``` 
- **Aggregate** (n8n-nodes-base.aggregate)
  Details:
    - **Notes**: ```plaintext
Combine records into one list``` 
