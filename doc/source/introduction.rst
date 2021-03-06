Introduction
============

This is the introduction to the early pre-alpha release of *mozaik* package.
*mozaik* is a integrated workflow framework for large scale neural simulations.
Note that currently it is under intense development, and anything can change
on daily basis. Alpha release of the package will follow soon.

It is built on top of following list of main tools:
    

    * pyNN (for definition and running of simulations)
    * neo  (for exchange and internal representation of data)
    * matplotib (for plotting)


*mozaik* currently covers following main areas of neural simulation workflow:
    
    * High-level components for definition of topologically organized spiking networks (built on top of `pyNN <http://neuralensemble.org/trac/PyNN/>`_)
    * Experiment control (description and execution of experiments, very basic so far)
    * Stimulus definition framework
    * Data storage (storage of recordings and analysis results)
    * Data manipulation (a query based system for performing high-level filtering operations over the datastore)
    * Analysis module
    * Plotting module

Tasks that we would like to cover in *mozaik* in future (any contributors welcome :-)!!!):
    
    * Support of FACETS like benchmarks within the Experimental control framework
    * Versioning system built on top of `Sumatra <http://neuralensemble.org/trac/sumatra/>`_
    * GUI for recording and anaylis browsing and plotting
    * Caching

*mozaik* is currently subdivided into 7 sub-packages:
    
    * :doc:`MozaikLite.framework` - contains the core of the *mozaik* package:
	
        * sheets - Code defining 2D sheets of neurons, one of the basic building blocks of *mozaik* networks
        * connectors - Defines various connections between sheets
        * experiment - Defines the experiment interface
        * experiment_controller - the control center of *mozaik* workflow
        * interfaces - collection of various basic *mozaik* interfaces
        * space - visual space handling

    * :doc:`MozaikLite.models` - code encapsulating a *mozaik* network consisting of sheets and connectors and providing
                                 'I/O' interface of it. Currently it also contains Retinal models (these might be reorganized in future).
                                 
    * :doc:`MozaikLite.stimuli` - definition of stimuli interface
    * :doc:`MozaikLite.storage` - data storage and data querying code
    * :doc:`MozaikLite.analysis` - analysis code
    * :doc:`MozaikLite.visualization` - plotting code
    

This might change as *mozaik* grows, and especially code in the framework 
is likely to get separated into new sub-package as it matures.

Following diagram offers intuition of how the control flows between the *mozaik* elements:


.. image:: mozaik_control_flow.png
