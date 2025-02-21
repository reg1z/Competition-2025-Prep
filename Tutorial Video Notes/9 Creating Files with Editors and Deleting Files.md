Video 9
https://www.youtube.com/watch?v=l0d7ks9ZkjU&list=PLqux0fXsj7x3WYm6ZWuJnGC1rXQZ1018M&index=9

- **Creating Files with Text Editors**
    - Running `nano <filename>` or `vi <filename>` on a non-existent file **creates a new file**.
    - Nano displays a warning when creating a file, while Vi requires entering **Insert Mode (`i`)** before adding text.
    - Saving in Nano: `Ctrl + X`, `Y`, `Enter`.
    - Saving in Vi: `Esc`, `:wq`, `Enter`.
- **Avoiding Common Mistakes**
    - Accidentally opening a **directory** in Nano or Vi produces a warning.
    - Using `Tab` for **auto-completion** prevents typos and accidental new file creation.
- **Deleting Files with `rm`**
    - `rm <filename>` removes a file permanently.
    - Can delete **multiple files** at once by listing filenames.
    - Running `rm` on non-existent files returns an error.