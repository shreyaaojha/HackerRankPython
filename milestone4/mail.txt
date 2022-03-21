
import smtplib
def mail():
    server = smtplib.SMTP('smtp.gmail.com:587')
    server.ehlo()
    server.starttls()
    server.ehlo()
    server.login('sender@mail.com','password')
    subject="mail"
    body="this program sends mails"
    message=f"Subject:{subject}\n\n{body}"
    server.sendmail('sender@mail.com','receiver@mail.com',message)
    print("mail sent")
    server.quit()
mail()
