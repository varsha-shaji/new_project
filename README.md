#!/bin/sh
#
# Git pre-commit hook example
# This hook checks if the README.md file exists.

if [ ! -f "README.md" ]; then
  echo "--------------------------------------------------------"
  echo "🚨 COMMIT REJECTED: Mandatory files are missing!"
  echo "Please create a README.md file before committing."
  echo "--------------------------------------------------------"
  # Exit with a non-zero status to abort the commit
  exit 1
fi

# If the check passes, the hook exits with 0 and the commit continues.
exit 0