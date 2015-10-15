# Introduction #

OpenDLP uses Perl-compatible regular expressions (PCREs) to find data residing on systems. This page is intended for everybody to contribute new regular expressions so they can eventually be integrated with each new release of OpenDLP. Leave a comment (or email me) and I will integrate them into the default list.

If you use the regular expression web interface of OpenDLP, you should not escape backslash "\" characters.  However, if you import them directly into MySQL, you must escape the backslash characters.  The regular expressions here do not contain escaped backslash characters.

For more information on PCREs, reference Wikipedia's entry at http://en.wikipedia.org/wiki/PCRE

# Regular Expressions #

```
Credit_Card_Track_1:(\D|^)\%?[Bb]\d{13,19}\^[\-\/\.\w\s]{2,26}\^[0-9][0-9][01][0-9][0-9]{3}
Credit_Card_Track_2:(\D|^)\;\d{13,19}\=(\d{3}|)(\d{4}|\=)
Credit_Card_Track_Data:[1-9][0-9]{2}\-[0-9]{2}\-[0-9]{4}\^\d
Mastercard:(\D|^)5[1-5][0-9]{2}(\ |\-|)[0-9]{4}(\ |\-|)[0-9]{4}(\ |\-|)[0-9]{4}(\D|$)
Visa:(\D|^)4[0-9]{3}(\ |\-|)[0-9]{4}(\ |\-|)[0-9]{4}(\ |\-|)[0-9]{4}(\D|$)
AMEX:(\D|^)(34|37)[0-9]{2}(\ |\-|)[0-9]{6}(\ |\-|)[0-9]{5}(\D|$)
Diners_Club_1:(\D|^)30[0-5][0-9](\ |\-|)[0-9]{6}(\ |\-|)[0-9]{4}(\D|$)
Diners_Club_2:(\D|^)(36|38)[0-9]{2}(\ |\-|)[0-9]{6}(\ |\-|)[0-9]{4}(\D|$)
Discover:(\D|^)6011(\ |\-|)[0-9]{4}(\ |\-|)[0-9]{4}(\ |\-|)[0-9]{4}(\D|$)
JCB_1:(\D|^)3[0-9]{3}(\ |\-|)[0-9]{4}(\ |\-|)[0-9]{4}(\ |\-|)[0-9]{4}(\D|$)
JCB_2:(\D|^)(2131|1800)[0-9]{11}(\D|$)
Social_Security_Number_dashes:(\D|^)[0-9]{3}\-[0-9]{2}\-[0-9]{4}(\D|$)
Social_Security_Number_spaces:(\D|^)[0-9]{3}\ [0-9]{2}\ [0-9]{4}(\D|$)
```