List Splitter
=============

Generic interface for splitting iterables into
smaller iterables, and for building basic grids.

USAGE
-----

    import list_splitter

    inp_dict = {
      'a': 1,
      'b': 2,
      'c': 3,
      'd': 4,
      'e': 5,
      'f': 6
    }

    inp_list = [
      1,
      2,
      3,
      4,
      5,
      6
    ]

    """
    Prints:

    [
      {'a': 1, 'b': 2, 'c': 3},
      {'d': 4, 'e': 5, 'f': 6}
    ]
    """
    print(list(list_splitter.n_chunks(inp_dict, 2)))

    """
    Prints:

    [
      [1, 2, 3],
      [4, 5, 6]
    ]
    """
    print(list(list_splitter.n_chunks(inp_list, 2)))

    """
    Prints:

    [
      {'a': 1, 'c': 3},
      {'b': 2, 'e': 5},
      {'d': 4, 'f': 6}
    ]
    """
    print(list(list_splitter.chunks_of_n(inp_dict, 2)))

    """
    Prints:

    [
      [1, 2],
      [3, 4],
      [5, 6]
    ]
    """
    print(list(list_splitter.chunks_of_n(inp_list, 2)))

    """
    Prints:

    [
      [{'a': 1}, {'c': 3}],
      [{'b': 2}, {'e': 5}],
      [{'d': 4}, {'f': 6}]
    ]
    """
    print(list(list_splitter.chunks_matrix(inp_dict, 1, 2)))

    """
    Prints:

    [
      [[1], [2]],
      [[3], [4]],
      [[5], [6]]
    ]
    """
    print(list(list_splitter.chunks_matrix(inp_list, 1, 2)))

    """
    Prints:

    [
      [{'a': 1, 'c': 3}],
      [{'b': 2, 'e': 5}],
      [{'d': 4, 'f': 6}]
    ]
    """
    print(list(list_splitter.chunks_matrix(inp_dict, 2, 1)))

    """
    Prints:

    [
      [[1, 2]],
      [[3, 4]],
      [[5, 6]]
    ]
    """
    print(list(list_splitter.chunks_matrix(inp_list, 2, 1)))

