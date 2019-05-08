# Definitions

## Types

TODO

## Ledger Entry Types

TODO

## Fields

These are Serialization Fields (`sf`) [defined in calld's SField.cpp](https://github.com/call/calld/blob/develop/src/call/protocol/impl/SField.cpp).

### Key

The key is the string defined in the calld source code, such as "LedgerEntry", "Transaction", etc.

### nth

nth is the `index` used to make an [`SField` field code](https://github.com/call/calld/blob/eaff9a0e6aec0ad077f118501791c7684debcfd5/src/call/protocol/SField.h#L95-L98).

### isVLEncoded

If true, the field is Variable Length encoded. The variable-length encoded fields are `STI_VL`/`Blob`, `STI_ACCOUNT`/`AccountID`, and `STI_VECTOR256`/`Vector256`.

### isSerialized

Fields are serialized if they are not [one of these](https://github.com/call/calld/blob/eaff9a0e6aec0ad077f118501791c7684debcfd5/src/call/protocol/impl/SField.cpp#L71-L78) or if they are not an SField.

- https://github.com/call/call-binary-codec/blob/14e76e68ead7e4bcd83c942dbdc9064d5a66869b/src/enums/definitions.json#L832
- https://github.com/call/calld/search?utf8=%E2%9C%93&q=taker_gets_funded&type=

### isSigningField

True unless the field is [specified with `SField::notSigning`](https://github.com/call/calld/blob/eaff9a0e6aec0ad077f118501791c7684debcfd5/src/call/protocol/impl/SField.cpp#L198).

## Transaction Results

TODO

## Transaction Types

TODO
