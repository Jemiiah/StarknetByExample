# Events

Events are a way to emit data from a contract. All events must be defined in the `Event` enum, which must be annotated with the `#[event]` attribute.
An event is defined as a struct that derives the `starknet::Event` trait. The fields of that struct correspond to the data that will be emitted. An event can be indexed for easy and fast access when querying the data at a later time by adding a `#[key]` attribute to a field member.

Here's a simple example of a contract that emits an event each time a counter is incremented by the `increment` function:

```cairo
// [!include ~/listings/getting-started/events/src/counter.cairo:contract]
```
