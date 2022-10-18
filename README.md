## OKP4 automatic rewards and stake

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
Account: kiwiwallet (local)
Address: okp41u376ksxhpytfm63rh699w6as95ekfk2mlx5ntr
======================================================
Account balance:      496259uknow
Available rewards:    1622392uknow
Net balance:          2118651uknow
Reservation:          100000uknow

You are about to delegate 2018651uknow to okp4valoper1u376ksxhpytfm63rh699w6as95ekfk2m2py64z:
```

### Customize settings (optional)
If you like, you can use your favorite text editor to change some of the default settings of the script.

```
##############################################################################
# User settings.
##############################################################################

KEYRING_BACKEND=file
MINIMUM_DELEGATION_AMOUNT="2000000"
RESERVATION_AMOUNT="100000"
VALIDATOR="okp4valoper1u376ksxhpytfm63rh699w6as95ekfk2m2py64z"

##############################################################################
# Sensible defaults.
##############################################################################

CHAIN_ID="okp4-nemeton"                                     # Current chain id. Empty means auto-detect.
NODE="tcp://localhost:27657"  					# Either run a local full node or choose one you trust.
OKP4BIN=okp4d
```

Take care to specify the `RESERVATION_AMOUNT` which is the minimum amount of uatoms that will remain available in your account.

You can delegate to any validator you prefer by changing `VALIDATOR` variable.