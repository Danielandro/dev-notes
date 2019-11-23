# Brace Expansion in Bash

Braces `{}` tell bash to do something the string(s) it finds in them.

This can be used to save time when creating multiple files in the same folder.

## Use Cases

### Create multiple files in the same directory

**Instead of:**

`touch /danny/projects/clock/components/Hours.js /danny/projects/clock/components/Minutes.js /danny/projects/clock/components/Seconds.js`

**Use:**

`touch /danny/projects/clock/components/{Hours,Minutes,Seconds}.js`

### Renaming a file

**Instead of:**

`mv /danny/projects/clock/components/Hours.js /danny/projects/clock/components/Decades.js`

**Use:**

`mv /danny/projects/clock/components/{Hours,Decades}.js`

---

[Main Page](../README.md)
