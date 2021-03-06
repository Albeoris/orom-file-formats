## Map Tile Record

 Size | Meaning
------|--------
 0x02 | `Tile Id`.

`Tile Id` is, in fact, a composite identifier,
which consists of terrainId, tileColumnId, and tileRowId.
In addition, it also contains a passability flag   

```
    bool IsPassable   => (((TileId & 0xFF00) / 0x100) & 0x20) != 0;
    byte TerrainId    => (byte) (((TileId & 0xFF00) / 0x100) & 0x03);
    byte TileColumnId => (byte) ((TileId & 0x00F0) / 0x10);
    byte TileRowId    => (byte) Math.Min(TileId & 0x0F, TerrainId != 2 ? 13 : 7);
```
