---
order: 14.2
version: 4.19.0
title:
  en-US: Order Expand Column with JSX style API
  zh-CN: 特殊列排序
---

## zh-CN

// TODO

## en-US

Using the JSX style API you can set the order of the expand column using `<Table.Column.EXPAND_COLUMN />`.

```tsx
import { Table } from 'antd';

const { Column } = Table;

const data = [
  {
    key: 1,
    name: 'John Brown',
    age: 32,
    address: 'New York No. 1 Lake Park',
    description: 'My name is John Brown, I am 32 years old, living in New York No. 1 Lake Park.',
  },
  {
    key: 2,
    name: 'Jim Green',
    age: 42,
    address: 'London No. 1 Lake Park',
    description: 'My name is Jim Green, I am 42 years old, living in London No. 1 Lake Park.',
  },
  {
    key: 4,
    name: 'Joe Black',
    age: 32,
    address: 'Sidney No. 1 Lake Park',
    description: 'My name is Joe Black, I am 32 years old, living in Sidney No. 1 Lake Park.',
  },
];

ReactDOM.render(
  <Table
    expandable={{
      expandedRowRender: record => <p style={{ margin: 0 }}>{record.description}</p>,
    }}
    dataSource={data}
  >
    <Column title="Name" dataIndex="name" key="name" />
    <Column.EXPAND_COLUMN />
    <Column title="Age" dataIndex="age" key="age" />
    <Column title="Address" dataIndex="address" key="address" />
  </Table>,
  mountNode,
);
```
