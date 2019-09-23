'''
Sometimes I look back at my own code and reflect on how poorly it was written.
When I began, my code would look much like EXAMPLE A, but now I'm perfectly 
capable of reading and writing code as seen in EXAMPLE C. Great! 

But how does that comfort level apply in a group enviornment, where someone else
might be maintaining my code? Would I fully understand EXAMPLE C if I wasnt the 
one who desigend it? 

Verbosity does not always equate to readability, likewise,
while advanced techniques have their place, they are not always best practice
'''

# ##################### - EXAMPLE A - ######################## #
	# here we have  very basic way to generate a list of drives	
alpha = ['A','B','C','D','E','F','G','H','I','J','K','L','M',
		 'N','O','P','Q','R','S','T','U','V','W','X','Y','Z']
def GenDrivesA():
	for a in alpha:
		g = str(glob('%s:\\'%(a)))
		if not g == '[]': 
			g = g.replace("['",'')
			g = g.replace(r":\\']",'')
			yield g
			
for drive in GenDrivesA():
	print('Type A:',drive)
# ############################################################ #



# ##################### - EXAMPLE B - ######################## #
	# Reducing time spent coding and rebosity
alpha = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ'
def GenDrivesB():	
	for dr in [glob('%s:\\'%(a)) for a in alpha if not glob('%s:\\'%(a)) == []]:
		yield str(dr).replace("['",'').replace(r":\\']",'')

for drive in GenDrivesB():
	print('Type B:',drive)
# ############################################################ #
	
	
	
# ##################### - EXAMPLE C - ######################## #
	# Going ham, this is useful to know, but is likely going 
	#  to be harder to maintain than above in most situations
def GenDrivesC(): yield str([dr for dr in [glob('%s:\\'%(a)) for a in alpha if not glob('%s:\\'%(a)) == []]]).replace("[['",'').replace(r":\\']]",'')

for drive in GenDrivesC():
	print('Type C:',drive)
# ############################################################ #
