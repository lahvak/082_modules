# Notes for problem authors

# Scientific notation

When using `contectScientificNotation.pl`, __always__ add regular multiplication.
We prefer to enter scientific notation with `*` rather than `x`, so that it
will work even in regular "Numeric" context.  This is what you want:

```Perl
Context("ScientificNotation");
Context()->operators->add(
         '*' => {precedence => 3, associativity => 'left', type => 'bin',
                    TeX => '\times ', class => 'ScientificNotation::BOP::x'},
    );
```

