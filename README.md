# smart-fridge

Let's set some goals:
- I want my fridge to know when I'm out of stuff
- I should be able to query what's left of any item
- What's missing should populate my weekly shopping list

# input

So I probably need to register items going in and out of the fridge to keep a neat state. I could scan the barcode with some device placed close to the fridge for quick beeps. Maybe a tablet (already has a camera) or a [cheap handheld scanner](https://tinyurl.com/2729mexv). Then I need to collect and persist that data somewhere.

# query

To be able to query fridge state I need user-friendly names of everything. Luckily ica has public api that [supports barcode lookups](https://github.com/svendahlstrand/ica-api/blob/master/api-referens.md#strekkodss%C3%B6kning). I took some samples from the fridge and found:
- Fruktdryck Hallon & granatäpple Proviva
- Läsk Coca-Cola
- D-vitamin Olja

Some of these things where bought at other stores than ica so their api seems to cover many things. Nice.

# shopping list

I could set some threshold for critical items like 7 liters of milk every sunday (shopping day) or as soon as an item goes below.

# problems

- what to do with big packaging? sodas that come in 6-pack. I can't scan the box because I'm not going to drink the box. When registering I have to scan individual items. Could work if no more than say 6 and scanning is painless.
- what to do about cheese?
