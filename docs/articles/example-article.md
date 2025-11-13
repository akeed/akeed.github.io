# Example Article: Markdown Features

*Published: November 13, 2025*

This is a sample article demonstrating various Markdown formatting features available in MkDocs Material.

## Headers

You can use headers from H1 to H6:

### This is H3
#### This is H4
##### This is H5

## Text Formatting

**Bold text** and *italic text* can be combined ***like this***.

You can also use ~~strikethrough~~ text.

## Lists

Unordered lists:

- Item 1
- Item 2
  - Nested item 2.1
  - Nested item 2.2
- Item 3

Ordered lists:

1. First item
2. Second item
3. Third item

## Code Blocks

Inline code: `print("Hello, World!")`

Code blocks with syntax highlighting:

```python
def factorial(n):
    """Calculate factorial recursively."""
    if n <= 1:
        return 1
    return n * factorial(n - 1)

print(factorial(5))  # Output: 120
```

## Blockquotes

> This is a blockquote.
> It can span multiple lines.
>
> — Anonymous

## Admonitions

!!! note
    This is a note admonition. It draws attention to important information.

!!! tip
    This is a tip that might be helpful for readers.

!!! warning
    This is a warning about something important to be aware of.

!!! info "Custom Title"
    You can customize the title of admonitions.

## Tables

| Feature | Supported | Notes |
|---------|-----------|-------|
| Markdown | ✓ | Full support |
| Code highlighting | ✓ | Multiple languages |
| Tables | ✓ | With alignment |
| Admonitions | ✓ | Multiple types |

## Links

[Link to Google](https://www.google.com)

[Link to another article](getting-started-with-mkdocs.md)

## Images

You can add images like this:

```markdown
![Alt text](image-url.png)
```

## Horizontal Rule

---

## Footnotes

Here's a sentence with a footnote[^1].

[^1]: This is the footnote content.

## Task Lists

- [x] Completed task
- [x] Another completed task
- [ ] Incomplete task
- [ ] Another incomplete task

## Conclusion

These are just some of the many formatting features available in MkDocs Material. Experiment with different elements to create engaging content!
