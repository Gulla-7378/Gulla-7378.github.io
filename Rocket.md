# ROCKET CODE #
What is rocket ?
Rocket consists of stages called Node, and it defines structure for node to run paralley or sequentially

Sample code to create Rocket
```scala 

class RocketNameextends RocketProvider {

    override def configure: RocketDefinition ={

        RocketBuilder("RocketName of rocket to be displayed in UI")
        .name("RocketName of the Pipeline")
        .description("Description")
        .globalArg("name","value")
        .parallelism(value)
        .node[Node1]("Node 1 name").children("Node 2 name")
        .node[Node2]("Node 2 name")..children("Node 3 name", "Node N name")
        .nodeArg("name","value")
        .node[Node N]("Node N name").children("Children Node Name")
        .finish()
    }
}
```

Attribute of RocketBuilder 
1.  name - Name of Rocket, type string
2. description - Description of rocket, type string
3. globalArg - One or many aruguments can passed with default value and used in any of nodes
4. Node - Node definition of ETL that can run independtily
5. finish() - This is last method and create RocketDefinition from RocketBuilder
'''' This is sample snippet, nodes can be executed either in serial or in parallel ''''' 