
# Tutorial Projects
- Apple iOS Dev training: https://developer.apple.com/tutorials/app-dev-training
- CodeAcademy: https://www.codecademy.com/learn/learn-swift
- CodeWithChris: https://codewithchris.com/swift-tutorial-complete/

# Documentation
- Swift Language: https://docs.swift.org/swift-book
- Human Interface Guidelines: https://developer.apple.com/design/human-interface-guidelines

# Open questions
- does Struct in swift function like class properties?
- what does the "some" keyword mean in swift
- is `->` a lambda expression in swift?
- what are swift casing conventions?
- how to swift equality operators work?
- does the self keyword work like "this" in JS?
- what is swift string interpolation syntax
- what is this funky foreach syntax
- What does `guard` keyword do?

# Observations
- init() functions like constructor()
- $0 and $1 are shorthands for arguments in a closure, zero indexed

## Video notes: Demystifying SwiftUI
- [link to video](https://developer.apple.com/videos/play/wwdc2021/10022/)
- Three elements that control how SwiftUI updates:
### Identity: which view needs to be presented (view identity)?
- explicit identity: assigning different names/ids etc to different elements to differentiate.
- structural identity: using relative arrangement (similar to using first child elements etc in CSS selection)
- reccomendation: try to stick with fewer views that adapt to different state data, preserves state, more elegant transitions
- anyviews destroy type information, so don't use them. Add back `@ViewBuilder` tag to add information back

### Lifetime: views change as data changes values, but they have a stable identity that does not change
- view values are different than view identities. They are stored so that they can be compared against new values to check for change, but then they are destroyed.
- you can't rely on view values persisting. 
- a view's **lifetime** is the duration of the **identity**
- state & stateobject are initialized at the top of the view to instruct the system what pieces of data need to be held for the lifetime of the View
- state is destroyed when the view disappears



