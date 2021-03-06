# Contract.Destroy method ()

Destruction of smart contracts. The smart contract issued to the chain can not be destroyed by the outside, and if the contract is to be destroyed, it needs to write the logic of its destruction when writing the contract.

Namespace: [Neo.SmartContract.Framework.Services.Neo](../../neo.md)

Assembly: Neo.SmartContract.Framework

## syntax

```c#
public static extern void Destroy()
```

## example

```c#
public class Contract1: FunctionCode
{
     public static void Main()
     {
         var height = Blockchain.GetHeight();
         var block = Blockchain.GetBlock(height);
         if (block.Timestamp > 1514736000) // Beijing time 2018-1-1
         {
             Neo.SmartContract.Framework.Services.Neo.Contract.Destroy();
         }
     }
}
```



[Return to superior](../Account.md)
