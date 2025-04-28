# fit3152-tutorial-05--network-analysis-solved
**TO GET THIS SOLUTION VISIT:** [FIT3152 Tutorial 05- Network Analysis Solved](https://www.ankitcodinghub.com/product/fit3152-data-analytics-tutorial-05-network-analysis-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;119401&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;FIT3152  Tutorial 05- Network Analysis Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
Pre-tutorial Activity

1. Explore the degree distribution of nodes in the network

2. Calculate network statistics to identify key players in the network. For example which node/player has the most hub potential in the network.

3. Identify and plot community groups in the network considering edge betweenness and greedy modularity optimization. Hint: Treat the graph as undirected.

Tutorial Activities

Download and install package functions using:

install.packages(c(“igraph”, “igraphdata”)) library(igraph) library(igraphdata)

Density

𝑑𝑒𝑛(𝑔) =

where (𝐸!( is number of edges,

(𝑉!( is number of vertices Clustering/transitivity coefficient

3𝜏 (𝑔)

𝑐𝑙𝑡(𝑔) =

where 3𝜏△(𝑔) is number of triangles, 𝜏3(𝑔) is number of connected triples

Closeness Centrality

Betweenness Centrality

is the number of shortest paths

between s and t, is the number of shortest paths between s and t passing through v

2 Two student groups are based on the friendship networks below.

Group 1 Group 2

C

c

(a) Calculate the following graph and vertex measures by hand for each group:

Degree Distribution

Betweenness

Closeness

Diameter

Draw the distance matrix and calculate Average Path Length

Draw the Adjacency Matrix

(b) Create each graph using the igraph package in R and check your answers.

Tips

3 A group of friends have the following network (data on Moodle as Friends.csv)

A B C D E F G H I J

A 0 1 1 1 0 1 1 1 1 1

B 1 0 1 0 1 1 1 1 0 1

C 1 1 0 1 0 0 1 1 0 1

D 1 0 1 0 1 0 0 0 0 0

E 0 1 0 1 0 1 1 1 1 1

F 1 1 0 0 1 0 1 1 0 0

G 1 1 1 0 1 1 0 0 1 1

H 1 1 1 0 1 1 0 0 1 1

I 1 0 0 0 1 0 1 1 0 0

J 1 1 1 0 1 0 1 1 0 0

Describe the network. Who is the most dominant member of the group?

(a) (b)

library(igraph) set.seed(999)

g &lt;- sample_smallworld(1, 100, 5, 0.03)

V(g)$label &lt;- NA

V(g)$size &lt;- 8 V(g)$color &lt;- “red”

h &lt;- erdos.renyi.game(100, 1/15)

V(h)$label &lt;- NA

V(h)$size &lt;- 8 V(h)$color &lt;- “red” par(mfrow=c(1,2))

plot(g, layout = layout.fruchterman.reingold) plot(h, layout = layout.fruchterman.reingold)

6 Use the following data and code to generate a basic graph.

library(“igraph”)

nodes &lt;- read.csv(“Dataset1-Media-Example-NODES.csv”, header=T, as.is=T) links &lt;- read.csv(“Dataset1-Media-Example-EDGES.csv”,header=T, as.is=T)

# Create Igraph object

net &lt;- graph_from_data_frame(d=links, vertices=nodes, directed=T) plot(net)

try and improve the plot, along the lines of the example given.

7 Create a random graph based on the scale-free Barabási-Albert model using the code below.

&gt; set.seed(9999)

&gt; BA &lt;- sample_pa(100)

Now create another graph according to Erdós-Rényi random graph model.

&gt; set.seed(9999)

&gt; ER &lt;- sample_gnm(100, 100)

Now create a Small World graph according to the Watts and Strogatz model.

&gt; set.seed(9999)

SW &lt;- sample_smallworld(1, 100, 5, 0.05)

(b) Which type of network has more powerful individuals with respect to their ability to control information flow in the network?

8 The file rfid contains encounter network data for staff in a hospital. Looking at the simplified network, describe the network and calculate summary statistics. Using the results of your analysis, identify the most important people in the network. Use the following code to create the data

&gt; library(igraph)

&gt; library(igraphdata)

&gt; data(rfid)

&gt; nrfid &lt;- rfid

&gt; nrfid &lt;- simplify(nrfid, remove.multiple = TRUE, remove.loops = TRUE,

+ edge.attr.comb = getIgraphOpt(“edge.attr.comb”))

&gt; plot(nrfid)

In the table above, an X indicates the attendance by a woman at an event. By treating each pair of women who attended the same event as being ‘connected’ and aggregating this over the 14 meetings construct a social network for the women using the following methods:

(a) Treat the graph as unweighted. That is, the number of meetings each pair of women attended is not counted (1 if the pair were present at any meeting and 0 otherwise), and

(b) Treat the graph as weighted. That is, each pair of women attending each meeting is counted. For example, the first pair of women (Jefferson and Mandeville) would have a weight of 6 since they both attended 6 meetings where the other was in attendance.

Analyse the data and describe the social network formed using both methods. Are there differences in your analysis for part (b) that become apparent using weighted edges.

For more information on the data see: http://svitsrv25.epfl.ch/R-doc/library/latentnet/html/davis.html

# To make a complete graph from a set of vertices # from https://igraph.org/r/doc/graph_from_literal.html gg = graph_from_literal(A:B:C:D:E:F:G — A:B:C:D:E:F:G)

# Make a second graph with some shared players hh = graph_from_literal(A:B:H:I:J — A:B:H:I:J)

# now make a union

# from https://igraph.org/r/doc/union.igraph.html ii = (gg %u% hh)

# make a data frame of people and club membership

Person = as.data.frame((c(“A”, “B”, “C”, “D”, “E”, “F”, “G”, “H”, “I”, “J”, “A”, “B”)))

Club = as.data.frame((c(“X”, “X”, “X”, “X”, “X”, “X”, “X”, “Y”, “Y”, “Y”, “Y”, “Y”)))

ClubData = cbind(Person, Club)

colnames(ClubData) = c(“Person”, “Club”) UniquePerson = unique(Person) colnames(UniquePerson) = “Person”

g &lt;- make_empty_graph(directed = FALSE)

# add vertices

for (i in 1 : nrow(UniquePerson)) {

g &lt;- add_vertices(g, 1, name = as.character(UniquePerson$Person[i])) }

# make complete graph for each club and add to g for (k in unique(ClubData$Club)){ temp = ClubData[(ClubData$Club == k),]

# combine each pair of agents to make an edge list

Edgelist = as.data.frame(t(combn(temp$Person,2))) colnames(Edgelist) = c(“P1”, “P2”)

# add edges

for (i in 1 : nrow(Edgelist)) { g &lt;- add_edges(g,

c(as.character(Edgelist$P1[i]),as.character(Edgelist$P2[i]))) }

# following line just to check groups are correct, not needed for graph print(temp)

} plot(g)

g = simplify(g)

plot(g)

Tips

10 The following graph shows an alleged insider trading network. Construct the directed graph in igraph and using your analysis identify who, in addition to Raj Rajaratnam, was an important player in the network. (You might want to enter your data into R as a directed graph formula (Slides 64, 65), using a two letter abbreviation for each person)

For more information on the data see:

https://www.valuewalk.com/2015/03/information-networks-evidence-from-illegal-insider-trading-tips/

g &lt;- graph.formula(J-+D, J++R, J+-A, A-+S, A++R, A-+M, S-+R)
