## Testing for Get Version

This is the testing repository for [warpkez/getversion](https://github.com/warpkez/getversion).

It runs three tests on the action:
```yml
      - name: Get Version from Tag
        id: getversion
        uses: warpkez/getversion@${version}
        with:
          version-format: 'with-v'
      
      - name: Use rel_version in workflow
        run: echo "The extracted rel_version is ${{ steps.getversion.outputs.rel_version }}"          
```

```yml
      - name: Get Version from Tag
        id: getversion
        uses: warpkez/getversion@${version}
        with:
          version-format: 'without-v'
      
      - name: Use rel_version in workflow
        run: echo "The extracted rel_version is ${{ steps.getversion.outputs.rel_version }}"          
```

```yml
      - name: Get Version from Tag
        id: getversion
        uses: warpkez/getversion@${version}

      - name: Use rel_version in workflow
        run: echo "The extracted rel_version is ${{ steps.getversion.outputs.rel_version }}"        
```