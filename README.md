
1. makemime  # encode e-mail's mime attachment
2. ripmime   # decode e-mail's mime attachment
3. w3m       # web browser to view html
4. file      # determine the type of a file
5. uuencode  # encode binary to ascii, suitabled for inclusion in an e-mail to serve as an attachment
6. uudecode  # decode ascii to binary
7. fetchmail # fetch e-mail from a remote mailbox
8. getmail   # fetch e-mail from a remote mailbox
9. msmtp     # send e-mail to a remote mailbox

    SMTP.domain.ORG
    SMTP 587 STARTTLS
    SMTP 465 SSL/TLS
    IMAP/POP.domain.ORG
    POP 110 STARTTLS
    POP 995 SSL/TLS

#encode file to mime format and append to e-mail
makemime -c text/html file >> e-mail
makemime -c application/pdf file >> e-mail
#decode file and place each decoded attachment into directory
ripmime -i file -d directory
#render and browse file as html
w3m -T text/html file
