email written in go
=====  

Email library for Go.  

Requires go version >= 1.1  

This is inspired by github.com/jordan-wright/email.  

## How to use it

```go
e := NewEmail()
e.FromName = "Katsuya Goto"
e.FromAddress = "test@gmail.com"
e.ToAddresses = []string{"test@example.com"}
e.BccAddresses = []string{"test_bcc@example.com"}
e.CcAddresses = []string{"test_cc@example.com"}
e.Subject = "Awesome Subject"
e.Text = []byte("Text Body is, of course, supported!\n")
e.HTML = []byte("<h1>Fancy Html is supported, too!</h1>\n")
e.Send("smtp.gmail.com:587", smtp.PlainAuth("", e.From(), "password123", "smtp.gmail.com"))
```
