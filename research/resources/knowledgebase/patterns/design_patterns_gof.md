# Knowledge Base: Patterns — Design Patterns (GoF)

**Synthesized from:** GoF, Design Patterns Explained, Intro to Design Patterns in C#

## Quick Reference

### Creational (5)
| Pattern | Intent |
|---------|--------|
| Abstract Factory | Interface for creating object families |
| Builder | Separate construction from representation |
| Factory Method | Let subclasses decide which class to instantiate |
| Prototype | Clone existing objects |
| Singleton | One instance, global access |

### Structural (7)
| Pattern | Intent |
|---------|--------|
| Adapter | Convert interface to expected one |
| Bridge | Decouple abstraction from implementation |
| Composite | Tree structure, uniform interface |
| Decorator | Attach responsibilities dynamically |
| Façade | Unified interface to subsystem |
| Flyweight | Share fine-grained objects efficiently |
| Proxy | Surrogate/placeholder for another object |

### Behavioral (11)
| Pattern | Intent |
|---------|--------|
| Chain of Responsibility | Pass request along handler chain |
| Command | Encapsulate request as object |
| Interpreter | Grammar + interpreter for language |
| Iterator | Sequential access without exposing representation |
| Mediator | Encapsulate object interaction |
| Memento | Capture/externalize state without violating encapsulation |
| Observer | One-to-many dependency, notify on change |
| State | Alter behavior when state changes |
| Strategy | Encapsulate interchangeable algorithms |
| Template Method | Algorithm skeleton, subclasses fill steps |
| Visitor | Operation on elements of object structure |

## 3 Design Principles

1. **Program to interface, not implementation**
2. **Favor composition over inheritance** (black-box > white-box reuse)
3. **Encapsulate what varies**

## Decision Matrix

| Problem | Pattern | Why |
|---------|---------|-----|
| Object creation varies | Factory Method / Abstract Factory | Encapsulate creation |
| One instance | Singleton | Global access point |
| Complex construction | Builder | Step-by-step |
| Interface mismatch | Adapter | Convert interface |
| Tree structure | Composite | Uniform interface |
| Add behavior dynamically | Decorator | Stack wrappers |
| Simplify subsystem | Façade | Clean interface |
| Algorithm varies | Strategy | Encapsulate variation |
| State-dependent behavior | State | State objects |
| One-to-many notification | Observer | Event handling |
| Request as object | Command | Undo/redo |
| Algorithm skeleton | Template Method | Subclass steps |

## Source Books
- GoF — definitive reference
- Design Patterns Explained — conceptual foundations
- Introduction to Design Patterns in C# — implementations
