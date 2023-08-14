# VI Editor
There are a number of text editors available in linux such as VI, VIM, NANO etc.

VI comes installed by default with most operating systems

### Open the file
```bash
vi index.html
```

**VI editor has two modes of operation:**

1. COMMAND MODE <span style='background: white; color: black; padding: 3px 7px; border-radius: 2px; margin: 0 4px;'>esc</span>
2. INSERT MODE <span style='background: white; color: black; padding: 3px 7px; border-radius: 2px; margin: 0 4px;'>i</span>

- When you open a file, you are by default in the command mode
- In command mode, you can copy, paste, delete a line or a word or to navigate between lines but you can not write contents to the file.
- to write content, you must switch to insert mode.

## Command mode Operations
1. Move Around <span style='background: white; color: black; padding: 3px 7px; border-radius: 2px; margin: 0 4px;'>Arrow keys</span>
2. Delete character <span style='background: white; color: black; padding: 3px 7px; border-radius: 2px; margin: 0 4px;'>x</span>
3. Delete the entire line <span style='background: white; color: black; padding: 3px 7px; border-radius: 2px; margin: 0 4px;'>dd</span>
4. Copy a line <span style='background: white; color: black; padding: 3px 7px; border-radius: 2px; margin: 0 4px;'>yy</span>
5. Paste it <span style='background: white; color: black; padding: 3px 7px; border-radius: 2px; margin: 0 4px;'>p</span>
6. Scroll up and down <span style='background: white; color: black; padding: 3px 7px; border-radius: 2px; margin: 0 4px;'>ctrl + u</span> <span style='background: white; color: black; padding: 3px 7px; border-radius: 2px; margin: 0 4px;'>ctrl + d</span> 

7. To Type Command <span style='background: white; color: black; padding: 3px 7px; border-radius: 2px; margin: 0 4px;'>:</span> 
8. Save <span style='background: white; color: black; padding: 3px 7px; border-radius: 2px; margin: 0 4px;'>:w</span> 
9. Quit (Discard) <span style='background: white; color: black; padding: 3px 7px; border-radius: 2px; margin: 0 4px;'>:q</span> 
10. Save + Quit <span style='background: white; color: black; padding: 3px 7px; border-radius: 2px; margin: 0 4px;'>:wq</span> 

11. Find (of word) <span style='background: white; color: black; padding: 3px 7px; border-radius: 2px; margin: 0 4px;'>/of</span> 
12. To move the cursor to the rest of occurrences <span style='background: white; color: black; padding: 3px 7px; border-radius: 2px; margin: 0 4px;'>n</span> 