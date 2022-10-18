## OKP4 automatic rewards and stake

[![Cosmos ecosystem][cosmos-shield]][cosmos-link]

The provided script enable delegators to claim all their staking rewards and reinvest them, to receive compounded interest.

### Installation

First download the script and make it executable:
```
curl -O https://raw.githubusercontent.com/Megavolv/okp4d-auto-rewards/master/reinvest.sh
chmod +x reinvest.sh
```

### Enjoy the show

The script has some default settings and only requires you to provide the name for the account you wish to work with.

The name must match the output of the NAME: column of `okp4d keys list`:  

You can now run the script:
```
./reinvest.sh testkey1 XxpasswordxX
```

and expect output such as:

```
======================================================
Account: testkey1 (local)
Address: okp4valoper1u376ksxhpytfm63rh699w6as95ekfk2m2py64z
======================================================
Account balance:   20000122217uknow
Available rewards: 23588169uknow
Net balance:       20023710386uknow
Reservation:       100000000uknow

You are about to delegate 19923710386uknow to okp4valoper1u376ksxhpytfm63rh699w6as95ekfk2m2py64z:

```

### Customize settings (optional)
If you like, you can use your favorite text editor to change some of the default settings of the script.

```
##############################################################################
# User settings.
##############################################################################

MINIMUM_DELEGATION_AMOUNT="2000000"
RESERVATION_AMOUNT="100000"
VALIDATOR="okp4valoper1u376ksxhpytfm63rh699w6as95ekfk2m2py64z"

##############################################################################
```

Take care to specify the `RESERVATION_AMOUNT` which is the minimum amount of uatoms that will remain available in your account.

You can delegate to any validator you prefer by changing `VALIDATOR` variable.