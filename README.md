# official-communities

This repository is used to collect the data for official communities on [Arena Social](https://arena.social) and [Arena Trade](https://arena.trade).

## How to Submit a New Official Community

To add a new official community, follow these steps:

1. Create a new directory in the `official-communities` folder with your contract address as the directory name (e.g., `0x1234...`)

2. Inside your directory, you need to provide two files:
   - `logo.png`: Your community logo (recommended size: 400x400px, can be square or circular)
   - `config.py`: Configuration file with the following parameters:
     ```python
     CONTRACT_ADDRESS='0x1234...'  # Must be lowercase
     PAIR_ADDRESS='0x5678...'      # Must be lowercase
     HANDLE='YourCommunityHandle'
     NAME='YOUR COMMUNITY NAME'
     TICKER='TICKER'
     DESCRIPTION='Your community description'
     OWNER_HANDLE='OwnerHandle'
     TOTAL_SUPPLY=total_supply_in_wei  # Example: 1e9 * 1e18 for 1 billion
     POSTING_THRESHOLD=threshold_in_wei  # Example: 1e6 * 1e18 for 1 million
     ```

3. Create a Pull Request (PR) with your changes:
   - Fork this repository
   - Create a new branch
   - Add your community directory with the required files
   - Submit a PR

4. PR Requirements:
   - Ensure all required files are present
   - Verify that the contract address matches the directory name
   - Check that the logo meets the size requirements
   - Confirm all config.py parameters are correctly filled out

5. After approval, your community will be added to both Arena Social and Arena Trade platforms.

## File Structure Example
```
official-communities/
└── 0x1234.../
    ├── logo.png
    └── config.py
```

## Important Notes
- Make sure your contract address is correct and matches the directory name
- The logo should be high quality and properly sized
- All config.py parameters are required
- The posting threshold should be reasonable for your community
- The total supply should be specified in wei (1e18 = 1 token)
- Contract and pair addresses must be in lowercase format
