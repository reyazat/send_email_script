# Send Email Script

This Bash script constructs an email with attachments and sends it using the `sendmail` command.

## Usage

1. Modify the variables at the beginning of the script to customize the email's details and attachments.

```bash
from="sender@example.com"
to="recipient@example.org"
subject="Some fancy title"
boundary="ZZ_/afg6432dfgkl.94531q"
body="This is the body of our email"
declare -a attachments
attachments=( "foo.pdf" "bar.jpg" "archive.zip" )
```

2. Execute the script.

```bash
./send_email.sh
```

## Prerequisites

- The `sendmail` command should be installed and properly configured on the system.

## Variables

- `from`: Email address of the sender.
- `to`: Email address of the recipient.
- `subject`: Subject of the email.
- `boundary`: Boundary string used for MIME parts.
- `body`: Body content of the email.
- `attachments`: Array containing paths to the attachments.

## Notes

- Ensure that the attachments specified in the `attachments` array actually exist in the specified paths before running the script.
- The `get_mimetype` function used to determine the MIME type of attachments is not provided in this script. You need to implement it separately or use an alternative method to determine the MIME type.
- The `sendmail` command is invoked with the flags `-t` and `-oi`, which allow sending the email using the standard input and preserve line breaks.

---

Make sure to include any additional information or instructions specific to your use case.