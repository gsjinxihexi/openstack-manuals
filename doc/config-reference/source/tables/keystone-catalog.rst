..
    Warning: Do not edit this file. It is automatically generated from the
    software project's code and your changes will be overwritten.

    The tool to generate this file lives in openstack-doc-tools repository.

    Please make any changes needed in the code, then run the
    autogenerate-config-doc tool from the openstack-doc-tools repository, or
    ask for help on the documentation mailing list, IRC channel or meeting.

.. _keystone-catalog:

.. list-table:: Description of catalog configuration options
   :header-rows: 1
   :class: config-ref-table

   * - Configuration option = Default value
     - Description
   * - **[catalog]**
     -
   * - ``template_file`` = ``default_catalog.templates``
     - (String) Absolute path to the file used for the templated catalog backend. This option is only used if the `[catalog] driver` is set to `templated`.
   * - ``driver`` = ``sql``
     - (String) Entry point for the catalog driver in the `keystone.catalog` namespace. Keystone provides a `sql` option (which supports basic CRUD operations through SQL), a `templated` option (which loads the catalog from a templated catalog file on disk), and a `endpoint_filter.sql` option (which supports arbitrary service catalogs per project).
   * - ``caching`` = ``True``
     - (Boolean) Toggle for catalog caching. This has no effect unless global caching is enabled. In a typical deployment, there is no reason to disable this.
   * - ``cache_time`` = ``None``
     - (Integer) Time to cache catalog data (in seconds). This has no effect unless global and catalog caching are both enabled. Catalog data (services, endpoints, etc.) typically does not change frequently, and so a longer duration than the global default may be desirable.
   * - ``list_limit`` = ``None``
     - (Integer) Maximum number of entities that will be returned in a catalog collection. There is typically no reason to set this, as it would be unusual for a deployment to have enough services or endpoints to exceed a reasonable limit.
