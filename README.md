![Static Badge](https://img.shields.io/badge/Template%20Version-V0.01-pink) ![Static Badge](https://img.shields.io/badge/Node-Tronscanapi-e84878) ![Static Badge](https://img.shields.io/badge/Node-SplitOut-e84878) ![Static Badge](https://img.shields.io/badge/Node-Filter-e84878) ![Static Badge](https://img.shields.io/badge/Node-HttpRequest-e84878) ![Static Badge](https://img.shields.io/badge/Node-ScheduleTrigger-e84878) ![Static Badge](https://img.shields.io/badge/Node-Aggregate-e84878) ![Static Badge](https://img.shields.io/badge/Node-templates-e84878)
![Static Badge](https://cdn.statically.io/gh/Automations-Project/n8n-templates/main/src/img/covers/n8n-usdt-and-trc20-wallet-tracker-api-workflow-for-n8n/idJRnUJqPb.png)

# USDT And TRC20 Wallet Tracker API Workflow for n8n

![70SJbNauXa.png](fileId:733)
## Overview

This n8n workflow is specifically designed to monitor USDT TRC20 transactions within a specified wallet. It utilizes the public blockchain database of TronScan, requiring no API authentication, to periodically check and process transaction data. This workflow is ideal for users who need an automated solution to track their TRC20 wallet transactions.

## Features

* **Automated Tracking**: Executes every 15 minutes to capture new transactions.
* **Customizable Filters**: Tailors the tracking based on specific parameters like transaction time and wallet addresses.
* **Data Aggregation**: Compiles transaction data into a single, structured list.
* **Formatted Outputs**: Presents transaction data in an organized and comprehensible format.

## Requirements

* N8N (self-hosted or cloud version) setup and operational.
* Basic understanding of N8N workflows and nodes.

## Setup and Configuration

1. **Import Workflow**: Load the provided JSON workflow into your N8N instance.
2. **Configure Edit Fields Node**:
 * Enter your TRC20 wallet address in the 'Your Wallet Address' field.
 * Adjust 'Number of transactions to retrieve per request' if necessary. (Default one set to 20 which is recommanded)
3. **TronScan Data Access**: The workflow accesses TronScan's public blockchain data, so no additional configuration is required for API access.
4. **Schedule Trigger Node**: Defaulted to trigger every 15 minutes. Modify as per your requirements.
5. **Test the Workflow**: Execute the workflow manually to ensure everything is operating correctly.

## How it Works

1. **Schedule Trigger**: Initiates the workflow at predetermined intervals.
2. **Edit Fields**: Sets up the wallet address and transaction retrieval count.
3. **TronScan Data Retrieval**: Gathers transaction data from the TRC20 wallet using TronScan's public database.
4. **Split Out & Filter**: Processes and filters the transaction data.
5. **Final Results**: Organizes and formats the required transaction data for review.
6. **Aggregate**: Consolidates all records (items) into a one comprehensive list (item).

![firefox_7ETdE2k8nJ.png](fileId:734)

## Customization

* Modify the filter conditions and fields to suit your tracking needs. (for example you can higher or lower the number of time to filter or IN / OUT transactions - Default is 15m/IN)
* Adjust the schedule trigger frequency according to your preference (default is 15m).

## Best Practices

* Regularly test the workflow to ensure consistent performance.
* Stay updated with any changes to the structure of TronScan's public data that might affect the workflow.

## Contributing

Your feedback and contributions are greatly appreciated. Feel free to adapt, modify, and share enhancements with the n8n community.

# Stats
[![N8N Creator Profile - Nskha](https://cdn.statically.io/gh/Automations-Project/n8n-templates/main/stats.min.svg)](https://n8n.io/creators/nskha)