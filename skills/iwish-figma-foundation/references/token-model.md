# Token Model

Start small and expand only when the page blueprint needs it.

## Collections

### Primitives

Raw brand, neutral, white/black, and state values. Use one mode.

### Semantic Color

Alias primitives rather than duplicating values:

```text
color/bg/default
color/bg/secondary
color/bg/inverse
color/text/primary
color/text/secondary
color/text/inverse
color/border/default
color/action/primary
color/action/secondary
color/state/success
color/state/error
```

### Spacing

```text
space/0  space/4  space/8  space/12  space/16
space/24 space/32 space/48 space/64 space/80 space/96
```

### Radius

```text
radius/0 radius/4 radius/8 radius/12 radius/16 radius/24 radius/full
```

## Typography styles

Create only styles required by the project while keeping a stable hierarchy:

```text
Display
Heading/H1
Heading/H2
Heading/H3
Heading/H4
Body/Large
Body/Medium
Body/Small
Label
Caption
```

Verify the actual brand/product font. Do not silently default to Inter.

