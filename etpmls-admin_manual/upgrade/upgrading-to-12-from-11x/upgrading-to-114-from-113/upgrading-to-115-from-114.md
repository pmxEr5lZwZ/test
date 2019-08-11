# Upgrading To 1.1.5 From 1.1.4

> app/Http/Controllers/Admin/MenuController.php  \#69

```
        //Get Menu Tree data
        $controller['tree'] = $this->menuRepository->getTreeData('- Top Menu -');
```



