An item will lose durability when:
* break a block will reduce 1 durability 
* damage a entity will reduce 1 durability 
* power triggered will reduce durability according to power.consumption (or some power specified way)
* armor be hit will reduce 1 durability

After event handled, if item's durability is below or equal 0, it will consume itself.

If the item have PowerUnbreakable, it won't lost its last 1 durability. When some tried to reduce durability more or equal to current durability, it will cancel the event (can't break blocks、 can't damage entities or fail to use powers but your armors will be hit as usual). 
