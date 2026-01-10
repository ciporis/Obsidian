### What event is

Event is just a call which is recieved by any method which needs the information.

```
public event Func<int, string, bool> OnAmountChanged;
```

In this case the event gives int, string and get bool from listeners

In general, we just declare which form of giving and recieving data we use.

#### Delegates

```
public delegate void Method(string name);
```

Delegate declares the signature of methods which are event's listeners.
### Action and UnityAction

```
public event Action<bool> DoorOpened;
public event UnityAction<int> MoneyAdded;
```
Разница только в количестве передаваемых аргументов

Action == null 
если на событие никто не подписан

### Event call

```
MoneyAdded?.Invoke()
```

# Code in Wallet class

```
public int Money { get; private set; }
public event UnityAction AmountChanged;

public void AddMoney(int amount)
{
	if(amount) <= 0
		return;
	Money += amount;

	AmountChanged?.Invoke();
}
```


# Code in WalletViewer class


```
public void OnEnable()
{
	_wallet.AmountChanged += DisplayAmount();
}

public void OnDisable()
{
	_wallet.AmountChanged -= DisplayAmount();
}

public void DisplayAmount()
{
	int amount = _wallet.Money;
	Debug.Log(amount.ToString());
}
```