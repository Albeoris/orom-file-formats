## Structure Record

 Size | Meaning
------|--------
 0x02 | `Id`. Identifier of an entry in structures section
 0x04 | (`X Coord` * 0x100) + 0x80 (sort of a fixed point value)
 0x04 | (`Y Coord` * 0x100) + 0x80 (sort of a fixed point value)
 0x04 | `Structure Id`. Points to a [Structure Kind](../../Enumerations/ALM/StructureKind.md)
 0x04 | `Fraction Id`. Value in a range `[1..16]` points to a fraction this structure belongs
 0x02 | `Health`. Condition of a structure in a range [0..100]
