email
=====  
Written in go.  
This is inspired by (forked from) [jordan-wright](https://github.com/jordan-wright/email).  


## Install
```c
// Requires go version >= 1.1  
go get github.com/gotokatsuya/email
```


## How to use it

```go
e := NewEmail()
e.FromName = "Katsuya Goto" // Kanji is OK too.
e.FromAddress = "test@gmail.com"
e.ToAddresses = []string{"test@example.com"}
e.BccAddresses = []string{"test_bcc@example.com"}
e.CcAddresses = []string{"test_cc@example.com"}
e.Subject = "Awesome Subject"
e.Text = []byte("Text Body is, of course, supported!\n")
e.HTML = []byte("<h1>Fancy Html is supported, too!</h1>\n")
e.Send("smtp.gmail.com:587", smtp.PlainAuth("", e.From(), "password123", "smtp.gmail.com"))
```
