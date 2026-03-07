# TapTitans2AlchemyCalculator

A .NET console application that calculates optimal alchemy crafting paths for Tap Titans 2.

## Running Locally

To run the application locally, you need to have the [.NET 8.0 SDK](https://dotnet.microsoft.com/download/dotnet/8.0) installed.

1. Clone the repository:
   ```bash
   git clone https://github.com/boxofyellow/TapTitans2AlchemyCalculator.git
   cd TapTitans2AlchemyCalculator
   ```

2. Run the application:
   ```bash
   dotnet run
   ```

   You can optionally specify a targeted reward as a command-line argument:
   ```bash
   dotnet run Wildcards
   ```

The application reads recipe data from `recipeData.csv` and inventory data from `inventoryData.csv` to calculate the optimal crafting plan.

## Using the Issue Template

You can request an alchemy calculation by creating a new issue using the **Alchemy Calculator Request** template.

[Create a new Alchemy Calculator Request](https://github.com/boxofyellow/TapTitans2AlchemyCalculator/issues/new?template=alchemy-calculator.yml)

Simply fill in your targeted reward and inventory data, and the calculator will run automatically when you submit the issue.

## Running the Calculator on a Pull Request

To run the Alchemy Calculator against the code in a pull request:

1. Add the `alchemy-calculator` label to the pull request.
2. Comment on the PR with your targeted reward and inventory data using the same format as the issue template:

   ```
   ## Targeted Reward
   Wildcards

   ## Inventory Data
   Ingredient,Quantity
   Leaf,5
   Sand,3
   ...
   ```

The workflow will check out the PR's head commit, build it, and post the results as a comment on the PR. This is useful for testing a branch's calculator logic with real inventory data before merging.
