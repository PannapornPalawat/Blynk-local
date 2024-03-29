#hardware mqtt port
hardware.mqtt.port=8440
#hardware ssl port
hardware.ssl.port=8441
#hardware plain tcp/ip port
hardware.default.port=8442
#http and web sockets port
http.port=8080
#https and web sockets port
https.port=9443
#application ssl port
app.ssl.port=8443
#address to bind to. by default bounded to all interfaces
listen.address=
#by default server uses embedded in jar cert to simplify local server installation.
#WARNNING DO NOT USE THIS CERTIFICATES ON PRODUCTION OR IN WHERE ENVIRNOMENTS REAL SECURITY REQUIRED.
#provide either full path to files either use '.' for specifying current directory. For instance "./myfile.crt"
server.ssl.cert=
server.ssl.key=
server.ssl.key.pass=
#by default System.getProperty("java.io.tmpdir")/blynk used
data.folder=
#folder for logs.
logs.folder=./logs
#log debug level. trace|debug|info|error. Defines how precise logging will be.
log.level=info
#maximum number of devices allowed per account
user.devices.limit=25
#maximum number of tags allowed per account
user.tags.limit=100
#defines maximum allowed number of user dashboards. Needed to limit possible number of tokens.
user.dashboard.max.limit=100
#defines maximum allowed widget size in KBs as json string.
user.widget.max.size.limit=20
#user is limited with 100 messages per second.
user.message.quota.limit=100
#maximum allowed number of notification queue. Queue responsible for processing email, pushes, twits sending.
#Because of performance issue - those queue is processed in separate thread, this is required due
#to blocking nature of all above operations. Usually limit shouldn't be reached.
notifications.queue.limit=5000
#Number of threads for performing blocking operations - push, twits, emails, db queries.
#Recommended to hold this value low unless you have to perform a lot of blocking operations.
blocking.processor.thread.pool.limit=6
#this setting defines how often we can send mail/tweet/push or any other notification. Specified in seconds
notifications.frequency.user.quota.limit=15
#this setting defines how often we can send webhooks. Specified in miliseconds
webhooks.frequency.user.quota.limit=1000
#this setting defines how big could be response for webhook GET request. Specified in kbs
webhooks.response.size.limit=72
#maximum size of user profile in kb's
user.profile.max.size=128
#number of strings to store in terminal widget
terminal.strings.pool.size=25
#number of strings to store in map widget
map.strings.pool.size=25
#number of strings to store in lcd widget
lcd.strings.pool.size=6
#maximum number of rows allowed
table.rows.pool.size=100
#period in millis for saving all user DB to disk.
profile.save.worker.period=60000
#period in millis for saving stats to disk.
stats.print.worker.period=60000
#specifies maximum period of time when hardware socket could be idle. After which
#socket will be closed due to non activity. In seconds. Default value 15 if not provided.
#leave it empty for infinity timeout
hard.socket.idle.timeout=15
#enable DB
enable.db=false
#enable raw data storage to DB
enable.raw.db.data.store=false
#size of async logger ring buffer. should be increased for loads >2-3k req/sec
async.logger.ring.buffer.size=2048
#initial amount of energy
initial.energy=10000000
#ADMINISTRATION SECTION
admin.rootPath=/admin
#used for reset password page and certificate generation.
#by default current server IP is taken. could be replaced with more friendly hostname.
#it is recommended to override this property with your server IP to avoid possible problems of host resolving
#server.host=test.blynk.cc
#email used for certificate registration, could be omitted in case you already specified it in mail.properties
#contact.email=
#network interface to determine server's current IP.
#only the first characters of the interface's name are needed.
#the default setting eth will use the first ethX interface found (i.e. eth0)
net.interface=eth
#comma separated list of administrator IPs. allow access to admin UI only for those IPs.
#you may set it for 0.0.0.0/0 to allow access for all.
#you may use CIDR notation. For instance, 192.168.0.53/24
allowed.administrator.ips=0.0.0.0/0,::/0
# default admin name and password. that will be created on initial server start
admin.email=admin@blynk.cc
admin.pass=admin
#comma separated list of users allowed to create accounts. leave it empty if no restriction required.
allowed.users.list=
