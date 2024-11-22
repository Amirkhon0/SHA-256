В CMD:
sha256.cmd 1231231 > sha.txt

В 1с:
ЗапуститьПриложение(sha256.cmd 1231231 > sha.txt)

Вариант 2: получения ответа прямо в 1с 
WshShell = Новый COMОбъект("Wscript.Shell");
WshExec = WshShell.Exec("cmd.exe /C ""sha256.cmd 1231231""");
    
OutStream = WshExec.StdOut;
Стр = OutStream.ReadAll();