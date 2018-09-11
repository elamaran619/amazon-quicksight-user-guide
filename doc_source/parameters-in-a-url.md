# Using Parameters in a URL<a name="parameters-in-a-url"></a>

The following example shows the URL action of a dashboard that opens another dashboard with the parameter "ASIN" set from the caller:

```
https://us-east-2.quicksight.aws.amazon.com/sn/dashboards/abc123-abc1-abc2-abc3-abcdefgh1234#p.myParameter=<<myValue>>
```

In the previous example, the first part of the URL is the link to the target dashboard: `https://us-east-2.quicksight.aws.amazon.com/sn/dashboards/abc123-abc1-abc2-abc3-abcdefgh1234`\.

We follow it with `#`, to introduce parameters\. Next, we provide the parameter name, `myParameter`, prefixed with `p.` to identify it as a parameter, rather than a field\. Then we use the equals sign `=` to set the parameter to field name, enclosed in angle brackets `<< >>`\. This sets it to the value in the field\. You can also set it to a literal value, without the angle brackets\. 

If you want send a parameter from one dashboard to another, tag it as a parameter by prefixing the value with a $\. For example:

```
https://us-east-2.quicksight.aws.amazon.com/sn/dashboards/abc123-abc1-abc2-abc3-abcdefgh1234#p.ManufacturerParentCode=<<$ParentAccount>>
```

**Note**  
Use the parameter's name, not the parameter control’s display name\. You can view the parameter name by opening the dashboard, and choosing **Parameter** on the left sidebar\.

In the following example, the is no `p. `prefix because `VendorCode` is a field, not a parameter\. Also, the value `{Store Code}` is enclosed in curly braces, because it contains a space\.

```
https://us-east-2.quicksight.aws.amazon.com/sn/dashboards/abc123-abc1-abc2-abc3-abcdefgh1234#StoreCode=<<{Store Code}>> 
```

**Warning**  
Avoid using a `?` after the dashboard link\. Using the `?` is a security risk\. Instead, use a hash `#`\.