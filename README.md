# All_OUT_OF_BOX
OUT_OF_BOX_SOLUTIONS


SELECT DISTINCT owner, object_type, object_name
FROM all_objects
WHERE object_type IN ('FUNCTION', 'PROCEDURE', 'PACKAGE', 'PACKAGE BODY', 'TRIGGER')
AND (INSTR(TEXT, '<<column_name>>') > 0 OR INSTR(TEXT, ':"column_name"') > 0)
ORDER BY owner, object_type, object_name;
