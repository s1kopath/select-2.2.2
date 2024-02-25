# Select 2.2.2 Dropdown

This repository contains an example of a select dropdown tree created using HTML, CSS, and jquery.

## Preview

<div>
  <img src="https://github.com/s1kopath/select2-tree/blob/main/preview.png?raw=true" title="Git" **alt="Git" />
</div>

## Dependencies

This example utilizes the following dependencies:

- [jQuery](https://jquery.com/)
- [Select2](https://select2.org/)

These dependencies are included via CDN links in the `index.html` file.

## Directory Structure
```code
.
├── index.html
├── README.md
└── .gitignore
```

## Uses

### head
```code
<link href="https://cdnjs.cloudflare.com/ajax/libs/select2/4.0.2-rc.1/css/select2.min.css" rel="stylesheet" />
```
### body
```code
<select id="mySelect"></select>
```
### script
```code
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/select2/4.0.1/js/select2.full.min.js"></script>
<script>
    $(document).on("ready", function () {
        var data = [{
            id: "2",
            text: "2 - Gastos",
            level: 1
        }, {
            id: "2.1",
            text: "2.1 - DESPESA OPERACIONAL FIXA",
            level: 2
        }, {
            id: "2.1.1",
            text: "2.1.1 - PESSOAL",
            level: 3
        }, {
            id: "2.1.1",
            text: "2.1.1 - PESSOAL",
            level: 4
        }, {
            id: "2.1.1.1",
            text: "2.1.1.1 - GERENCIA/ADMINSTRATIVO",
            level: 4
        }, {
            id: "2.1.1.1.1",
            text: "2.1.1.1.1 - SALÁRIOS",
            level: 5
        }, {
            id: "2.1.1.1.2",
            text: "2.1.1.1.2 - DIVIDENDOS / COMISSÕES /BONUS",
            level: 5
        }, {
            id: "2.1.1.1.3",
            text: "2.1.1.1.3 - INSS",
            level: 5
        }, {
            id: "2.1.1.1.4",
            text: "2.1.1.1.4 - FGTS",
            level: 5
        }];

        function formatResult(node) {
            var $result = $('<span style="padding-left:' + (20 * node.level) + 'px;">' + node.text + '</span>');
            return $result;
        };

        $("#mySelect").select2({
            placeholder: 'Select an option',
            width: "600px",
            data: data,
            formatSelection: function (item) {
                return item.text
            },
            formatResult: function (item) {
                return item.text
            },
            templateResult: formatResult,
        });
    });
</script>
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Author

This example was created by [Md. Asaduzzaman](https://github.com/s1kopath).

