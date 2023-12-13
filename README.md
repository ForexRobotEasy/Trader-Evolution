# Trader Evolution - ReadMe

This ReadMe file provides information about the code for the Trader Evolution program developed by Forex Robot Easy Team. 

## Description

Trader Evolution is a program that facilitates forex trading by providing money management tools, technical analysis functions, and wave counting capabilities. The program is designed to optimize forex trading with unique tools and strategies.

## Money Management

The program includes a money management feature that allows users to choose between two methods: percentage-based calculation and fixed lot calculation. The `MM_Method` enum defines these methods.

### Percentage-Based Calculation

To use the percentage-based calculation method, the user can set the desired risk percentage per trade using the `SetPercentage` function. The program will calculate the trading volume based on the account balance and the specified risk percentage.

### Fixed Lot Calculation

Alternatively, the user can choose the fixed lot calculation method by setting a fixed lot size using the `SetFixedLot` function. In this case, the trading volume will remain constant regardless of the account balance.

## Usage Example

The code provided in the usage example demonstrates how to use the Trader Evolution program:

1. First, create an instance of the `TraderEvolution` class.
2. Set the desired money management method using the `SetMoneyManagementMethod` function.
3. If using the percentage-based calculation method, set the risk percentage using the `SetPercentage` function.
4. Calculate the trading volume based on the account balance using the `CalculateVolume` function.
5. Print the calculated volume.

```cpp
void OnStart()
{
    // Create an instance of TraderEvolution
    TraderEvolution trader;

    // Set Money Management Method
    trader.SetMoneyManagementMethod(PERCENTAGE);

    // Set Percentage for Percentage-Based Calculation
    trader.SetPercentage(2.5); // 2.5% risk per trade

    // Calculate Trading Volume
    double accountBalance = AccountInfoDouble(ACCOUNT_BALANCE);
    double volume = trader.CalculateVolume(accountBalance);

    // Print the calculated volume
    Print('Trading Volume: ', volume);
}
```

## Developer's Site

Please note that Forex Robot Easy Team is not the official developer of this product. This code is provided as a sample that can work as described in the product. For detailed reviews and trading results of this product, please visit the official developer's site: [Trader Evolution Review - Optimize Forex Trading with Unique Tools](https://forexroboteasy.com/forex-robot-review/trader-evolution-review-optimize-forex-trading-with-unique-tools/).

For more information about the Trader Evolution program and to find the official developer, please use MQL5.
