# ROCKET CODE #

''''' CODE SNIPPET ''''''

class RocketProviderName extends RocketProvider {

    override def configure: RocketDefinition ={

        RocketBuilder("Name of rocket to be displayed in UI")
        .name("Name of the Pipeline")
        .description("Description")
        .globalArg("name","value")
        .parallelism(value)
        .node[Node 1]("Node 1 name")
        .node[Node 2]("Node 2 name")
        .nodeArg("name","value")
        .
        .
        .
        .node[Node N]("Node N name").children("Children Node Name")
        .finish()
    }
}


'''' This is sample snippet, nodes can be executed either in serial or in parallel ''''' 