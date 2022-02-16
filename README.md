client.on("ready", async() => {
  let servers = await client.guilds.cache.size
  let servercount = await client.guilds.cache.reduce((a,b) => a+b.memberCount, 0 )

const activities = [
  `>help | ${servers} servers`,
  `Watching ${servercount} members`
]

setInterval(()=>{
const status = activities[Math.floor(Math.random()*activities.length)]
client.user.setPresence({ activities : [{name : `${status}`}]})
  
}, 5000)

})









