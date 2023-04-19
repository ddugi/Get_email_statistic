# Define the shared mailbox email address
$SharedMailbox = "youremai@domain.xx"

# Get the number of sent and received emails
$SentEmails = (Get-MessageTrace -SenderAddress $SharedMailbox -StartDate (Get-Date).AddDays(-10) -EndDate (Get-Date) -PageSize 5000 | Where-Object {$_.Status -eq "Delivered"}).Count
$ReceivedEmails = (Get-MessageTrace -RecipientAddress $SharedMailbox -StartDate (Get-Date).AddDays(-10) -EndDate (Get-Date) -PageSize 5000 | Where-Object {$_.Status -eq "Delivered"}).Count

# Display the results
Write-Host "Sent emails: $SentEmails"
Write-Host "Received emails: $ReceivedEmails"
