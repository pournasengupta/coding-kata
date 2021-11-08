## Kata 17: More Business Rules
> The rules that specify the overall processing of an order can be complex too, particularly as they often involve waiting around for things to happen.
> 
>>- If we accept an order over the web, then we have to wait for payment to arrive, unless it’s a credit-card order. In the case of credit card orders, we can process the order immediately and ship the goods, but only if the goods are in stock. If they are not currently in stock, we have to delay processing credit card orders until the become available again.
>>- We can receive a check in payment of an existing order, in which case we ship the goods (unless they are not in stock, in which case we hold the check until the goods become available).
>>- We can receive a purchase order (PO) for a new order (we only accept these from companies with an established credit account). In this case we ship the goods (assuming they are in stock) and also generate an invoice against the PO. At some point in the future we’ll receive payment against this invoice and the order will be complete.
>>- At any time before the goods are shipped the customer may cancel an order.
>
> Each step in this process may occur many days after the previous step. For example, we may take an order over the web on Monday, receive a check for this order on Thursday, then ship the goods and deposit the check when the item is received from our own suppliers on the following Tuesday.
>
> How can we design an application to support these kinds of rules? Of course, businesses change the rules all the time, so we better make sure that anything we come up makes it easy to update the workflow.
>
> Now you’re faced with implementing this system. The rules are complicated, and fairly arbitrary. What’s more, you know that they’re going to change: once the system goes live, all sorts of special cases will come out of the woodwork.





