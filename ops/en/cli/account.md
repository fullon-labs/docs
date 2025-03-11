# Account

{% hint style="info" %}
**Good to know:** FullOn protocol supports abstract accounts that all other digital assets or on-chain permissions are associated with.
{% endhint %}

## newaccount

Register an account name with a public key. The account name must contain exactly **12** characters from the base32 set: `., 1-5, a-z` with 13th character, if applicable, encoded in base16 using characters: `., 1-5, a-j`. It also must start with a lowercase letter `a-z` and must not end in a dot `.` character.

```shell

```shell
## CLI
tcli system newaccount $creator $acct $pubkey -p ${creator}@active

```

## get account balance

```shell
## CLI
tcli get currency balance $token_contract $account $symbol

```