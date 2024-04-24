# complex_networks_2024_1
Codes developed in the Complex Networks 2024.1

https://snap.stanford.edu/data/

https://networkx.org/

https://networkx.org/documentation/stable/auto_examples/index.html#examples-gallery

https://igraph.org/

http://networksciencebook.com/

https://diegomariano.com/networkx/

https://www.kaggle.com/code/flaviagg/grafos-em-python

https://cambridge-intelligence.com/keylines-faqs-social-network-analysis/

https://cambridge-intelligence.com/social-network-analysis/

https://medium.com/@tushar_aggarwal/networkx-a-comprehensive-guide-to-mastering-network-analysis-with-python-fd7e5195f6a0

https://github.com/tushar2704?tab=repositories

https://github.com/sna-unipi/SNA_lectures_notebooks.git

https://networkx.org/documentation/stable/reference/algorithms/assortativity.html

https://towardsdatascience.com/computing-assortativity-coefficients-on-a-social-network-dataset-7f65796feb70

https://ona-book.org/gitbook/


%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

Rascunho

# círculo com 6 nós
CG = nx.circulant_graph(6 ,[1])
nx.draw_kamada_kawai(CG, with_labels = True)

# grafo regular com 6 nós e 3 arestas por nó
RRG = nx.random_regular_graph(3, 6)
nx.draw_kamada_kawai(RRG, with_labels = True)

# grafo completo com 6 nós
CG6 = nx.complete_graph(6)
nx.draw_kamada_kawai(CG6, with_labels = True)

# karate club graph
KCG = nx.karate_club_graph()
nx.draw_kamada_kawai(KCG, with_labels = True)

# Grafo direcionado
DIG = nx.DiGraph ()

# Lista de nós
DIG.add_nodes_from(['a', 'b', 'c', 'd', 'e', 'f'])

# Arestas
DIG.add_edge('a', 'c')
DIG.add_edge('b', 'c')
DIG.add_edge('c', 'e') 
DIG.add_edge( 'c', 'f')
DIG.add_edge('d', 'e')
DIG.add_edge('d', 'f')

pos = nx . circular_layout (DIG)
pos['a'] = [ -1 ,0]
pos['b'] = [+0 ,0]
pos['c'] = [ -0.5 , -0.5]
pos['d'] = [+1.5 , -0.5]
pos['e'] = [+0.0 , -1.0]
pos[ 'f'] = [+1.0 , -1.0]

#larg = [(0.5*DIG[u][v]['peso']) for u , v in DIG.edges]
nx.draw_networkx(DIG , 
                 pos = pos, 
                 node_size = 1000, 
                 with_labels = True, 
                 arrows = True)
#nx.draw_kamada_kawai(DIG, with_labels = True)


