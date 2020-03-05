---
layout: post
title: "Collapsible Markdown"
tags: collapsible markdown
date: 2020-03-05
---

![Markdown image](https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcTAiDeNPS8fX3qEoEQlNrJ-kracnaTcp0Osdr5KpOUqcjkTo1-X)

 <details><summary>
  Markdown between html tags works when there's an empty line before it.
  </summary>
  here ```it doesn't work```

  here ```it works```

  </details>

Source:

```
 <details><summary>
  Markdown between html tags works when there's an empty line before it.
  </summary>
  here ```it doesn't work```

  here ```it works```

  </details>
```

[Full article](https://gist.github.com/joyrexus/16041f2426450e73f5df9391f7f7ae5f)

## collapsible markdown?

<details><summary>

# CLICK ME
</summary>
<p>

#### yes, even hidden code blocks!

```python
print("hello world!")
```

Source code:
```
## collapsible markdown?

<details>
<summary>

# CLICK ME
</summary>
<p>

#### yes, even hidden code blocks!

  ```python
  print("hello world!")
  ```
```
