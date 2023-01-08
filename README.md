# Painel_IFC+Revit

Painel de consulta de elementos e tipos enumerados em IFC e as BuiltInCategory de Revit 2023

As BuiltInCategory de Revit são um dos meios de filtragem decategorias de Revit que pode ser utilizada em mecanismos e APIs programadas com diversos fins 
em Revit O método embaixo ilustra um exemplo de uso. 

public IList<Element> Filtra_Elementos ( BuiltInCategory bic )    
{
       Document                 doc = rev.ActiveUIDocument.Document;
       FilteredElementCollector col = new FilteredElementCollector( doc );
       ElementCategoryFilter    fil = new ElementCategoryFilter   ( bic );
       IList<Element>           Lis = col.WherePasses(fil).WhereElementIsNotElementType().ToElements().ToList();                    
       return Lis;
}

![Painel_IFC_Revit](https://user-images.githubusercontent.com/9437020/211205667-23e508a1-f6da-4b0b-a568-ed71d344e228.PNG)
