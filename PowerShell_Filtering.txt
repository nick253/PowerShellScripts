Get-Service | 
Where-Object -FilterScript {$_.StartType -EQ 'Automatic'} |
Where-Object -Property Name -Cmatch "Win"

Get-Service |
	Where-Object {($_.Status -notcontains 'Running') -and ($_.StartType -in 'Manual')}