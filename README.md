# Python-API-Challenge Code Sources

**From Learning Assistant**

    hover_cols = ["Hotel Name", "Country"]

**From Professor**

    (%s)" % time.strftime("%Y-%m-%d") 
    
    #create liner regression graph function to be used repetitively for each graph above; prep to run each scattor again based on northern vs southern hemisphere 
    def liner_regression_plot(x_values, y_values, y_title, text_coordinates):

    #Set up linear regression
    (slope, intercept, rvalue, pvalue, stderr) = linregress(x_values, y_values)
    regress_values = x_values * slope + intercept
    line_eq = "y = " + str(round(slope,2)) + "x + " + str(round(intercept,2))

    #plotting properties
    plt.scatter(x_values,y_values)
    plt.plot(x_values,regress_values,"r-")
    plt.annotate(line_eq,text_coordinates,fontsize=15,color="red")
    plt.xlabel("Latitude")
    plt.ylabel(y_title)
    print(f"The r-value is: {rvalue**2}")
    plt.show()
