% tss2_setappdata(1) tpm2-tools | General Commands Manual
%
% APRIL 2019

# NAME

**tss2_setappdata**(1)

# SYNOPSIS

**tss2_setappdata** [*OPTIONS*]

# DESCRIPTION

**tss2_setappdata**(1) - This command allows an application to associate an arbitrary data blob with a given object. The data is stored and can be returned with tss2_getappdata. Previously stored data is overwritten by this function. If empty data is passed in, the stored data is deleted.

# OPTIONS

These are the available options:

  * **-p**, **\--path** _STRING_:

    Path of the object for which the appData will be stored.

  * **-i**, **\--appData** _STRING_:

    The data to be stored. Optional parameter. If omitted, stored data is deleted.

[common tss2 options](common/tss2-options.md)

# EXAMPLE

```
tss2_setappdata --path HS/SRK/myRSACrypt --appData appData
```

# RETURNS

0 on success or 1 on failure.

[footer](common/footer.md)
