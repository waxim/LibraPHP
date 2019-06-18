# LibraPHP

Allows you to communicate with a running Libra instance.

```
$connection = new Libra\Connection(env("LIBRA_ADDRESS");

# Add an account to libra
$alice = new Libra\Account();
$bob = new Libra\Account();

# Mint some coints
$result = new Libra\Mint(Money::unit(1000));

# Have alice send bob 50 Libra
$transaction = $alice->send(50, $bob, ($blocking = true));

echo "Alice has {$alice->balance} \n";
echo "Bob has {$bob->balance}";
```