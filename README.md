#!/bin/bash

# Define an array of strings to iterate over
strings=("string1" "string2" "string3")

# Loop over each string in the array
for str in "${strings[@]}"; do
  # Execute the shell script in the background with the current string as an argument
  /path/to/your/shell/script.sh "$str" &
done

# Wait for all background processes to finish
wait



# All_OUT_OF_BOX
OUT_OF_BOX_SOLUTIONS


SELECT DISTINCT owner, object_type, object_name
FROM all_objects
WHERE object_type IN ('FUNCTION', 'PROCEDURE', 'PACKAGE', 'PACKAGE BODY', 'TRIGGER')
AND (INSTR(TEXT, '<<column_name>>') > 0 OR INSTR(TEXT, ':"column_name"') > 0)
ORDER BY owner, object_type, object_name;

SELECT *
FROM all_dependencies
WHERE referenced_name = '<table_name>'
AND referenced_type = 'TABLE'
AND type IN ('PACKAGE', 'PACKAGE BODY', 'FUNCTION', 'PROCEDURE', 'TRIGGER', 'VIEW');

