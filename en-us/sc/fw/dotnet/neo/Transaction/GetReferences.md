# Transaction.GetReferences method ()

Query the transaction output referenced by all inputs of the current transaction.

Namespace: [Neo.SmartContract.Framework.Services.Neo](../../neo.md)

Assembly: Neo.SmartContract.Framework

## syntax

```c#
public extern Neo.SmartContract.Framework.Services.Neo.TransactionOutput[] GetReferences ()
```

Return Value: The transaction output referenced by all inputs for the current transaction, [TransactionOutput](../TransactionOutput.md).

## example

```c#
public class Contract1: FunctionCode
{
     public static void Main ()
     {
         byte[] transaction = new byte[] {88, 114, 160, 206, 130, 137, 41, 94, 119, 120, 242, 71, 232, 244, 3, 20, 165, 69, 182, 106, 185, 119, 239, 183, 65, 174, 220, 157, 251, 28, 215};
         Transaction tx = Blockchain.GetTransaction (transaction);
         TransactionOutput[] references = tx.GetReferences ();
     }
}
```



[Return to superior](../Transaction.md)
