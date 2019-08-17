# GotoLineCol-NPP-PythonScript
_A PythonScript implementation to navigate to desired line and column position in Notepad++ files_

### Utility
1. Moves the cursor position to the specified line and column for a file in Notepad++.
Especially useful for inspecting data files in fixed-width record format.

2. Also, displays the character code in decimal and hex at the specified position.

#### Customizable Parameters for the goToLineCol function call in main()

*bRepeatPrompt*: Whether to repeat prompting when the specified number value is out of range

*iEdgeBuffer*: Ensures that the caret will be that many characters inside the left and right edges of the editor viewing area, when possible

*iCaretHiliteDuration*: Caret will be in Block mode for specified seconds

*bCallTipAutoHide*: Whether to hide the call tip automatically in sync when caret highlighting is turned off

*bBraceHilite*: Whether to use brace highlighting style for the character at the specified position. Automatically turns off when current line changes.

#### Known Issues
1. Character code display in the call tip is functional with SBCS (Single-Byte Character Sets) and LTR (left-to-right) direction. With MBCS (Bulti-Bytes Character Sets) or RTL (right-to-left) direction, results will not be reliable.

2. If _iCaretHiliteDuration_ is set to a high value (>3 seconds), and the user tries to rerun the script while the previous execution is still running, the PythonScript engine will display an error message: "Another script is still running..." So set this parameter to 3 seconds or lower.
