# Simple Group

```java
SimpleGroupController simpleGroupController = client.getSimpleGroupController();
```

## Class Name

`SimpleGroupController`


# Get Calculate

Calculates the expression using the specified operation.

```java
CompletableFuture<Double> getCalculateAsync(
    final GetCalculateInput input)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `operation` | [`OperationTypeEnum`](/doc/models/operation-type-enum.md) | Template, Required | The operator to apply on the variables |
| `x` | `double` | Query, Required | the LHS value |
| `y` | `double` | Query, Required | the RHS value |

## Response Type

`double`

## Example Usage

```java
GetCalculateInput getCalculateInput = new GetCalculateInput();
getCalculateInput.setOperation(OperationTypeEnum.SUBTRACT);
getCalculateInput.setX(222.14);
getCalculateInput.setY(165.14);

simpleGroupController.getCalculateAsync(getCalculateInput).thenAccept(result -> {
    // TODO success callback handler
}).exceptionally(exception -> {
    // TODO failure callback handler
    return null;
});
```

