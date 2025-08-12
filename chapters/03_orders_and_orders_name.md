# Chapter 3: Orders and Order Properties

In financial markets, traders use different types of orders to buy or sell securities. These orders come with specific instructions that determine **when** and **how** the trade will be executed.

---

## 3.1 Order Types

### Market Orders
- **Definition:** An instruction to buy or sell immediately at the best available price.
- **Key Feature:** Priority is given to **speed**, not price.
- **Use Case:** When you want to enter or exit a position quickly.
- **Risk:** Possible slippage in fast-moving markets.

---

### Limit Orders
- **Definition:** An instruction to buy or sell at a specific price or better.
- **Key Feature:** Priority is given to **price**, not speed.
- **Buy Limit Order:** Executes only at or below the specified price.
- **Sell Limit Order:** Executes only at or above the specified price.
- **Risk:** The order may not be filled if the market doesn’t reach your price.

---

### Stop Orders
- **Stop-Market Order:** Becomes a market order once a specified trigger price is reached.
- **Stop-Limit Order:** Becomes a limit order once the stop price is reached.
- **Use Case:** Often used to protect against large losses (stop-loss) or to enter a trade when the price moves past a certain level (stop-entry).

---

## 3.2 Order Properties

Orders often have **time and execution constraints**.

### Time-in-Force Instructions
- **Day Order:** Expires at the end of the trading day if not executed.
- **Good-'Til-Canceled (GTC):** Remains active until explicitly canceled.
- **Immediate-or-Cancel (IOC):** Executes all or part immediately, cancels the rest.
- **Fill-or-Kill (FOK):** Must be executed in full immediately, or it’s canceled.

---

### Other Instructions
- **All-or-None (AON):** The order must be executed completely or not at all.
- **Discretionary Order:** Gives the broker flexibility to improve execution.
- **Iceberg Order:** Only a small portion of the total order is visible in the order book.

---

## 3.3 Order Execution Priority

In most markets, orders are matched using a **price–time priority** system:
1. **Best Price:** Higher bid prices are executed before lower bid prices, and lower ask prices before higher asks.
2. **Earliest Time:** If multiple orders have the same price, the one placed earlier has priority.

---

## 3.4. Practical Considerations

- **Market orders** provide quick execution but may face poor fills in illiquid markets.
- **Limit orders** control price but risk missing execution.
- **Stop orders** help automate risk management but can be triggered by short-term price spikes.
- **Execution strategies** depend on market conditions, liquidity, and urgency.

---

**Key Takeaways:**
- Choosing the right order type is a balance between execution speed, price control, and risk tolerance.
- Time-in-force and special instructions can help align orders with specific trading strategies.
- Understanding market microstructure improves order placement efficiency.

