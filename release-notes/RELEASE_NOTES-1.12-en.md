# October 2021 - Version 1.12.0


# That's fixed

- The VAT is correctly recomputed in several corner cases:
    - when we change a billing group type to CESSION (margin is then adapted as well),
    - when a VAT exonerated vehicle's buyer is changed,
    - when a vehicle sale is initiated from the dealer file with a VAT exonerated contact.
- After editing or overriding vehicle prices, changes are visible when we go back to the catalog.
- After editing a vehicle dealer file or vehicle instance, changes are visible when we go back to the list.
