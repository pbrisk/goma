
--------
Tutorial
--------

.. toctree::


First setup basic objects
=========================

Setup model imports

    >>> from exactmatch import ExactMatch

For a simple example generate a nested list of match details

    >>> detail_list = [["Property1","Value1_2"],["Property2","Value2_2"],["Property3","Value3_2"]]
	
and a mapping list as instruction for the mapping algorithm

	>>> mapping_list = [["Property1","Property2","Property3","Target"], \
                        ["Value1_1","Value2_1","Value3_1","Target1"], \
                        ["Value1_2","Value2_2","Value3_2","Target2"]]

Finally generate an :py:class:`exactmatch.ExactMatch` instance

	>>> exact_match = ExactMatch()

and run the matching algorithm
	
    >>> exact_match.match(detail_list, mapping_list)
	"Target2"
