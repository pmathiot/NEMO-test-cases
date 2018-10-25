
# Isomip demonstration case
Here a description of the test case + link toward the src and notebooks. 
<br>
We here provide a physical description of this experiment and additional details as to how to run this experiment within NEMO. This experiment is **created and tested** for NEMO **code at revision 10193**. 

A **ipython notebook is also provided** as a demonstration of possible analysis. If you have already run the NEMO experiment and want to analyse the resulting output, you can directly look at the notebook : **[here](https://github.com/pmathiot/NEMO-test-cases/tree/master/isomip/notebook/isomip_notebook.ipynb)**.

## Objectives
Simple box configuration with an ice shelf covering all the domain. South part is a sloping ice shelf and north part is a flat ice shelf. The purpose of this test case is to evaluate the impact of various schemes and new development with the iceshelf cavities. This configuration served as initial assesment of the ice shelf module in Losh et al. (2008) and Mathiot et al. (2017).

## Physical description
The ISOMIP demonstration case follows the specifications described in details **[here](http://staff.acecrc.org.au/~bkgalton/ISOMIP/test_cavities.pdf)**.

### Exemple of run
In this exemple we assess the behaviour of the ....<br>

* The **Reference Simulation** : **FCT2** is the first simulation, ....

```
cd TEST_CASES/........
ln -sf namelist_....._cfg namelist_cfg
```
choice of..... is done in namtra_.... block of namelist: 

~~~fortran
!-----------------------------------------------------------------------

~~~

Run the executable : (if you haven't compiled NEMO see [here](https://github.com/sflavoni/NEMO-test-cases) )

``` 
 mpirun -np 1 ./opa 
```
Output files are: <br>

~~~

~~~

* The **Sensibility Simulation** : .


```
ln -sf namelist_xxxx_cfg namelist_cfg
```

Run the executable again : 

``` 
 mpirun -np 1 ./opa 
```

Output files : <br>

~~~

~~~

* You can change output file name  in variable @expname@ in file\_def\_nemo-opa.xml

~~~xml
<file_definition type="multiple_file" name="@expname@" sync_freq="10d" min_digits="4">
~~~

* Available notebook python is **[here](https://github.com/pmathiot/NEMO-test-cases/tree/master/isomip/notebook/isomip_notebook.ipynb)**.

## References
Losch, M., 2008: Modeling ice shelf cavities in a z coordinate ocean general circulation model, J. Geophys. Res.-Oceans, 113, C08043.
Mathiot, P., Jenkins, A., Harris, C., and Madec, G., 2017: Explicit representation and parametrised impacts of under ice shelf seas in the z* coordinate ocean model NEMO 3.6, Geosci. Model Dev., 10, 2849-2874.
