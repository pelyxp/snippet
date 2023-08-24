
snippet
sed -i 's/VARCHAR2(32767)/VARCHAR2(32000)/g' yashan_140_table*.sql
sed -i 's/FLOAT(126)/NUMBER(38)/g' yashan_140_table*.sql
sed -i 's/FLOAT(53)/NUMBER(38)/g' yashan_140_table*.sql
sed -i 's/CHAR(1)/BOOLEAN/g' yashan_140_table*.sql
sed -i 's/ COMPUTE STATISTICS//g' yashan_140_table_*.sql
sed -i  '/SUPPLEMENTAL LOG GROUP/d; /SUPPLEMENTAL LOG DATA/d' yashan_140_table*.sql
sed -i ':a;N;$!ba;s/,\s*\n\s*)/\n)/g'  yashan_140_table_*.sql
sed -i  's/NO INMEMORY (.*) ;/;/' yashan_140_table_only*.sql
sed -i  '/NO INMEMORY (.*)/d' yashan_140_table_seg*.sql
sed -i  '/NO INMEMORY (.*)/d' yashan_140_table_full*.sql
sed -i 's/DEFERRABLE//g' yashan_140_table_only_cons_SZWGOP.sql
sed -i 's/NOCOMPRESS//g'  yashan_160_index_not_cons_SZWGOP.sql
sed -i 's/BANKDISKFLAG BOOLEAN,/BANKDISKFLAG CHAR(1),/g' *.sql
