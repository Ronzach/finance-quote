**HOWTO use this module**

I modified the Tdefunds.pm module of Finance::Quote

To use it git clone https://github/ronzach/finance-quote 

git checkout fix-support-for-tdefunds

In order to use the updated TDefunds with Gnucash you need to modify 
the gnc-fq-dump and gnc-fq-helper scripts from your gnucash install

In those scripts comment out check_modules function call and replace with

```
#check_modules ();
use lib '/path/to/finance-quote/lib';
use Finance::Quote;
```

