# MemoCash-Fixes
Two fixes for mysql :)

We tested memo.cash on local machine and got two serirous errors

#1 Error 1366: Incorrect string value: '\xCB\x88s\xCA\x8C\xC9...' for column 'message' at row 1
#2 Error 1406: Data too long for column 'lock_string' at row 1 

We want to share our own fixes, so you can fix fix longer memo´s and other things ...

#1 Fix:
```ALTER TABLE memo_posts CONVERT TO CHARACTER SET utf8mb4;```

#2 Fix: 
```ALTER TABLE `transaction_outs` MODIFY `lock_string` LONGTEXT```

Fixes are for: ```https://github.com/memocash/memo```

Njoy!
