- name: Install dependencies
        run: npm ci
        working-directory: ./3dapp

      - name: Build project
        run: npm run build
        working-directory: ./3dapp

      - name: Upload artifact
        uses: actions/upload-pages-artifact@v3
        with:
          path: './3dapp/dist'
