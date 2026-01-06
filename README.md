# notes-to-doc

This project converts markdown meeting notes into a well-formatted Google Doc using the Google Docs API.

## Features
- Creates a Google Doc programmatically
- Converts markdown headings:
  - `#` → Heading 1
  - `##` → Heading 2
  - `###` → Heading 3
- Preserves nested bullet hierarchy with indentation
- Converts `- [ ]` into Google Docs checkboxes (with fallback if unsupported)
- Styles @mentions (bold + blue)
- Styles footer info (italic + gray + smaller font)

## Requirements
- Google Colab (recommended)
- Python 3
- Dependencies:
  - google-api-python-client
  - google-auth-httplib2
  - google-auth-oauthlib

## How to Run in Colab
1. Open `meeting_notes_to_gdoc.ipynb` in Google Colab.
2. Run the Auth cell (it will prompt you to sign in).
3. Run the notebook cells in order.
4. The output prints a Google Docs link.

## Notes
- This uses `https://www.googleapis.com/auth/documents` scope.
- If checkbox bullet preset isn't supported in the runtime, the script falls back to standard bullets.
