
0. To reproduce issue execute 

    `helm template umbrella  --set "global.ingress.annotations.test=global"`
    
    Both dep1 and dep2 ingresses will have `some-annotation: dep2` 
    
    When override global for every dependency it work as expected:
    
    `helm template umbrella --set "dep1.global.ingress.annotations.test=global" --set "dep2.global.ingress.annotations.test=global"`
